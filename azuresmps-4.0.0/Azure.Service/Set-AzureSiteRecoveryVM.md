---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105754"
---
# <span data-ttu-id="5c522-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="5c522-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="5c522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c522-102">SYNOPSIS</span></span>
<span data-ttu-id="5c522-103">Site kurtarma koruma varlığının kurtarma tarafı seçeneklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c522-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="5c522-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c522-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5c522-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c522-105">DESCRIPTION</span></span>
<span data-ttu-id="5c522-106">**Set-AzureSiteRecoveryVM** cmdlet 'ı, Azure Site Recovery koruma varlıkları için kurtarma sanal makine boyutu ve kurtarma sanal makine ağı gibi kurtarma tarafı koruma seçeneklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c522-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="5c522-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c522-107">EXAMPLES</span></span>

### <span data-ttu-id="5c522-108">Örnek 1: korumalı bir sanal makinede güncelleştirmeye Izin verme</span><span class="sxs-lookup"><span data-stu-id="5c522-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="5c522-109">İlk komut, korumalı bir kapsayıcı almak için **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanır ve ardından $ProtectionContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5c522-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="5c522-110">İkinci komut, **Get-AzureSiteRecoveryVM** cmdlet 'ini kullanarak $ProtectionContainer sanal makineleri alır ve $VitrualMachines değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5c522-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="5c522-111">Final komutu, NewVirtualMachine05 adlı $VitrualMachines dizisindeki ilk sanal makine için güncelleştirmelere izin verir.</span><span class="sxs-lookup"><span data-stu-id="5c522-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="5c522-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c522-112">PARAMETERS</span></span>

### <span data-ttu-id="5c522-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c522-113">-Name</span></span>
<span data-ttu-id="5c522-114">Hedef sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c522-114">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c522-115">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="5c522-115">-PrimaryNic</span></span>
<span data-ttu-id="5c522-116">Birincil ağ bağdaştırıcı kartını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c522-116">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c522-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="5c522-117">-Profile</span></span>
<span data-ttu-id="5c522-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c522-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c522-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5c522-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c522-120">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="5c522-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="5c522-121">Kurtarma ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c522-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c522-122">-Boyut</span><span class="sxs-lookup"><span data-stu-id="5c522-122">-Size</span></span>
<span data-ttu-id="5c522-123">Hedef sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c522-123">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c522-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5c522-124">-VirtualMachine</span></span>
<span data-ttu-id="5c522-125">Site kurtarma sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c522-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c522-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c522-126">CommonParameters</span></span>
<span data-ttu-id="5c522-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c522-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c522-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c522-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c522-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c522-129">INPUTS</span></span>

## <span data-ttu-id="5c522-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c522-130">OUTPUTS</span></span>

## <span data-ttu-id="5c522-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c522-131">NOTES</span></span>

## <span data-ttu-id="5c522-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c522-132">RELATED LINKS</span></span>

[<span data-ttu-id="5c522-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5c522-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="5c522-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="5c522-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


