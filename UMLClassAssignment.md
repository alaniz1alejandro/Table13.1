```mermaid
classDiagram
  class VideoGameCharacter {
    - name: string
    - health: int
    - armor: int
    + VideoGameCharacter(name: string, health: int, armor: int)
    + getName(): string
    + getHealth(): int
    + getArmor(): int
    + setName(name: string): void
    + setHealth(health: int): void
    + setArmor(armor: int): void
    + attack(target: VideoGameCharacter): void
    + takeDamage(damage: int): void
    + useAbility(ability: string): void
  }

  class MasterChief {
    + energyShield: int
    + meleeDamage: int
    + MasterChief(name: string, health: int, armor: int, energyShield: int, meleeDamage: int)
    + getEnergyShield(): int
    + getMeleeDamage(): int
    + setEnergyShield(energyShield: int): void
    + setMeleeDamage(meleeDamage: int): void
    + meleeAttack(target: VideoGameCharacter): void
    + throwGrenade(target: VideoGameCharacter): void
    + useArmorAbility(): void
  }

  class Arbiter {
    + energySwordDamage: int
    + cloakDuration: int
    + Arbiter(name: string, health: int, armor: int, energySwordDamage: int, cloakDuration: int)
    + getEnergySwordDamage(): int
    + getCloakDuration(): int
    + setEnergySwordDamage(damage: int): void
    + setCloakDuration(duration: int): void
    + energySwordAttack(target: VideoGameCharacter): void
    + activateCloak(): void
    + useSpecialAbility(): void
  }

  VideoGameCharacter <|-- MasterChief
  VideoGameCharacter <|-- Arbiter
