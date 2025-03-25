import numpy as np
import matplotlib.pyplot as plt

def gaussian_beam_waist(z, w0, lambda_):
    z_r = np.pi * w0**2 / lambda_
    return w0 * np.sqrt(1 + (z/z_r)**2)

z = np.linspace(-10, 10, 500)
w0 = 1.0  # Beam waist
lambda_ = 0.6328  # Wavelength in microns
w = gaussian_beam_waist(z, w0, lambda_)

plt.plot(z, w)
plt.xlabel("Propagation Distance (z)")
plt.ylabel("Beam Waist (w)")
plt.title("Gaussian Beam Propagation")
plt.show()
