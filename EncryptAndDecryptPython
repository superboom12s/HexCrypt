from random import *

alphabet = 'öööööööööööööööö0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZºª?¿¡!|@·#$~%&¬/()=^’*`+¨´ç,.-[]{};:_ qwertyuiopasdfghjklzxcvbnmáéíóúÁÉÍÓÚÑñ'
            #16

def findCharPosition(char):
    return alphabet.index(char)

def splitOnTwo(texto):
    #divide la entrada en una lista de tres en tres caracteres
    resultado = [texto[i:i + 2] for i in range(0, len(texto), 2)]
    return resultado

import math

def originalLenght(longitud_procesada):
    a = 1
    b = 1
    c = -2 * longitud_procesada
    discriminante = b**2 - 4*a*c
    if discriminante >= 0:
        sol1 = (-b + math.sqrt(discriminante)) / (2 * a)
        sol2 = (-b - math.sqrt(discriminante)) / (2 * a)
        return int(max(sol1, sol2))


def addMet(text):
    preProc2 = []
    #encuentra el caracter en el alfabeto y pasa su
    #posicion a hexadecimal
    preProc2 = hex(text)
    # separa el valor anterior en una lista de 4 elementos
    preProc2 = [*preProc2]
    # elimina los dos primeros elementos
    preProc2.pop(0)
    preProc2.pop(0)
    return ''.join(preProc2)

def encryp(text):

    preProc = []

    for symbol in range(len(text)):
        preProc.append(addMet(findCharPosition(text[symbol])))

    addrange = sorted(range(len(text)+1), reverse=True)
    iterVar = 1

    for i in range(len(text)):

        for j in range(addrange[i]):
                       #
            preProc.insert(iterVar, addMet(randint(29, 141)))
            iterVar += 1
        iterVar += 1

    return ''.join(preProc)

def decryp(text):

    postProc = splitOnTwo(text)

    addrange = sorted(range(originalLenght(len(postProc)) + 1), reverse=True)
    iterVar = 1

    for i in range(originalLenght(len(splitOnTwo(text)))):

        for j in range(addrange[i]):
            try:
                postProc.pop(iterVar)
            except:
                break

        iterVar += 1

    for i in range(len(postProc)):
        try:
            postProc[i] = alphabet[int(postProc[i], 16)]
        except:
            break

    return ''.join(postProc)
