--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying NOT NULL,
    galaxy_type character varying(30),
    milkyway_satellite boolean,
    color character varying
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying NOT NULL,
    planet_id integer,
    moon_orbit numeric,
    rover boolean
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying NOT NULL,
    star_id integer,
    planet_order integer,
    year_length numeric,
    rover boolean
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: rover; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.rover (
    rover_id integer NOT NULL,
    name character varying NOT NULL,
    age integer
);


ALTER TABLE public.rover OWNER TO freecodecamp;

--
-- Name: rover_rover_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.rover_rover_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.rover_rover_id_seq OWNER TO freecodecamp;

--
-- Name: rover_rover_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.rover_rover_id_seq OWNED BY public.rover.rover_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying NOT NULL,
    galaxy_id integer,
    star_age integer,
    color text
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: rover rover_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.rover ALTER COLUMN rover_id SET DEFAULT nextval('public.rover_rover_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', 'SBbc', NULL, NULL);
INSERT INTO public.galaxy VALUES (2, 'Canis Major', 'Irr', true, NULL);
INSERT INTO public.galaxy VALUES (3, 'Draco II', 'Dwarf', true, NULL);
INSERT INTO public.galaxy VALUES (4, 'Tucana III', 'Dwarf', true, NULL);
INSERT INTO public.galaxy VALUES (5, 'Sagittarius Dwarf', 'dSph', true, NULL);
INSERT INTO public.galaxy VALUES (6, 'Hydrus I', 'Dwarf', true, NULL);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'Moon', 3, 27, NULL);
INSERT INTO public.moon VALUES (2, 'Deimos', 4, 1, NULL);
INSERT INTO public.moon VALUES (3, 'Phobos', 4, 1, NULL);
INSERT INTO public.moon VALUES (4, 'Lo', 5, 2, NULL);
INSERT INTO public.moon VALUES (5, 'Europa', 5, 4, NULL);
INSERT INTO public.moon VALUES (6, 'Callisto', 5, 5, NULL);
INSERT INTO public.moon VALUES (7, 'Dia', 5, 12, NULL);
INSERT INTO public.moon VALUES (8, 'Euanthe', 5, 4, NULL);
INSERT INTO public.moon VALUES (9, 'Cyllene', 5, 77, NULL);
INSERT INTO public.moon VALUES (10, 'Carme', 5, 98, NULL);
INSERT INTO public.moon VALUES (11, 'Carpo', 5, 23, NULL);
INSERT INTO public.moon VALUES (12, 'Ersa', 5, 9, NULL);
INSERT INTO public.moon VALUES (13, 'Ganymede', 5, 66, NULL);
INSERT INTO public.moon VALUES (14, 'Harpalyke', 5, 34, NULL);
INSERT INTO public.moon VALUES (15, 'Herse', 5, 34, NULL);
INSERT INTO public.moon VALUES (16, 'Hegemone', 5, 2, NULL);
INSERT INTO public.moon VALUES (17, 'Kore', 5, 17, NULL);
INSERT INTO public.moon VALUES (18, 'Kalyke', 5, 18, NULL);
INSERT INTO public.moon VALUES (19, 'Himalia', 5, 19, NULL);
INSERT INTO public.moon VALUES (20, 'Kallichore', 5, 22, NULL);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Mercury', 1, 1, 88, NULL);
INSERT INTO public.planet VALUES (2, 'Venus', 1, 2, 225, NULL);
INSERT INTO public.planet VALUES (3, 'Earth', 1, 3, 365, NULL);
INSERT INTO public.planet VALUES (4, 'Mars', 1, 4, 687, NULL);
INSERT INTO public.planet VALUES (5, 'Jupiter', 1, 5, 4333, NULL);
INSERT INTO public.planet VALUES (6, 'Saturn', 1, 6, 10759, NULL);
INSERT INTO public.planet VALUES (7, 'Uranus', 1, 7, 30687, NULL);
INSERT INTO public.planet VALUES (8, 'Neptune', 1, 8, 60190, NULL);
INSERT INTO public.planet VALUES (9, 'Ceres', 1, NULL, 1682, NULL);
INSERT INTO public.planet VALUES (10, 'Pluto', 1, NULL, 90560, NULL);
INSERT INTO public.planet VALUES (11, 'Haumea', 1, NULL, 18, NULL);
INSERT INTO public.planet VALUES (12, 'Makemake', 1, NULL, 306, NULL);


--
-- Data for Name: rover; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.rover VALUES (1, 'Curiosity', 2011);
INSERT INTO public.rover VALUES (2, 'Perseverence', 2020);
INSERT INTO public.rover VALUES (3, 'Spirit', 2003);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'Sol', 1, 5, NULL);
INSERT INTO public.star VALUES (2, 'UY Scuti', 1, 3, NULL);
INSERT INTO public.star VALUES (3, 'RW Cephei', 1, 19, NULL);
INSERT INTO public.star VALUES (4, 'V354 Cephei', 1, NULL, NULL);
INSERT INTO public.star VALUES (5, 'KY Cygni', 1, 942, NULL);
INSERT INTO public.star VALUES (6, 'Mu Cephei', 1, 100, NULL);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 6, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 20, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 12, true);


--
-- Name: rover_rover_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.rover_rover_id_seq', 3, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 6, true);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: rover rover_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.rover
    ADD CONSTRAINT rover_name_key UNIQUE (name);


--
-- Name: rover rover_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.rover
    ADD CONSTRAINT rover_pkey PRIMARY KEY (rover_id);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: galaxy unique_g; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT unique_g UNIQUE (galaxy_id);


--
-- Name: moon unique_m; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT unique_m UNIQUE (moon_id);


--
-- Name: planet unique_p; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT unique_p UNIQUE (planet_id);


--
-- Name: star unique_s; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT unique_s UNIQUE (star_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

