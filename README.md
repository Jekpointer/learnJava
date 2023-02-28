public class Main {
    public static void main(String[] args) {


        Car bmw = new EngineCar("BMW", 120, 150, CarType.Sedan);
        Car tesla = new ElectroCar("Tesla", 100, 1200, CarType.Sedan);
        Car vw = new EngineCar("Volkswagen", 240, 2200, CarType.Pickup);
        Car mers = new EngineCar("Mercedes", 240, 2100, CarType.Offroad);

        testCar(bmw);
        testCar(tesla);
        testCar(vw);
        testCar(mers);
    }

    public static void testCar(Car car) {
        System.out.println("Hi! I'm " + car.getName() + "\n" +
                "My power is " + car.getPower() + "\n" +
                "My weight is " + car.getWeight() + "\n" +
                "i'm " + car.getCarType());
        //сделать вывод в консоль двигатель, заглушить и тд...
        car.getEngine().startEngine();
        car.startDrive();
        car.getWheel().rollWheel();
        car.stopDrive();
        car.getEngine().stopEngine();


    }
}
