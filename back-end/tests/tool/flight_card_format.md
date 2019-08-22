<!--
Load the necessary libraries
>> require_relative '../../tool/filter_and_sort_functions_for_segments.rb'
<...>

-->

### Cargamos los segmentos

Primero obtenemos los itnierarios de un Json normalizado, el cual contiene 54 segmentos totales en la
primera columna.
```ruby
>> data = JSON.parse(File.read('flights_data_examples/flights.json'))
>> segments = get_segments(data)
>> p segments.size
54
```
Por razones practicas del test, seleccionaremos el primero, ya que todos tienen el mismo formato.
```ruby
>> segment = segments.first
>> pp segment
{:airlines=>["American Airlines"],
 :arrival_time=>"2019-04-16T22:28:00",
 :departure_time=>"2019-04-16T21:00:00",
 :duration=>"PT1H28M",
 :flight_numbers=>["1455"],
 :from=>"Dallas",
 :price=>28150,
 :stops=>0,
 :to=>"New Orleans",
 :zid=>"ZFS-WEB-AA1455-DFW-MSY-1555466400-SUAIZNM1-S"}

```