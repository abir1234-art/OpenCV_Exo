# OpenCV_Exo
traitement_images_with_opencv
#!python --version
!python --version



import cv2

img = cv2.imread("architect.png")
print(img)

#cv2.imshow("mon image", img)

import matplotlib.pyplot as plt
img = cv2.imread("architect.png")
imgr = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(imgr)
plt.axis("off") #désactiver axe y et x
plt.show()

from skimage import io
import matplotlib.pyplot as plt

image = io.imread('architect.png')
plt.imshow(image)
plt.show()

import cv2
#from skimage import io
import matplotlib.pyplot as plt
# charger l'image
image = cv2.imread('architect.png')
# appliquer un flou gaussien (taille du noyau 5*5)
flou_image = cv2.GaussianBlur(image, (5,5), 0)
plt.imshow(image)
plt.show()
#afficher l'image floutée
#cv2.imshow('Flou Gaussien', flou_image)
#sauveagrder l'image floutée
cv2.imwrite('architect.png', flou_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
