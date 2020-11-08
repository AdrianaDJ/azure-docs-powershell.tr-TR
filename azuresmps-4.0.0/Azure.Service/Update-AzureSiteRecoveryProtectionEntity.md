---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106015"
---
# <span data-ttu-id="faba9-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="faba9-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="faba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faba9-102">SYNOPSIS</span></span>
<span data-ttu-id="faba9-103">Azure Site Recovery 'de bir koruma varlığının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="faba9-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="faba9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="faba9-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="faba9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="faba9-105">DESCRIPTION</span></span>
<span data-ttu-id="faba9-106">**Update-AzureSiteRecoveryProtectionEntity** cmdlet 'ı Azure Site Recovery 'de sanal makine sahibi bilgileri gibi bir koruma varlığının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="faba9-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="faba9-107">Bu cmdlet yalnızca sanal makine Izleyicisi (VMM) için VMM korumalı koruma varlıklarına desteklenir.</span><span class="sxs-lookup"><span data-stu-id="faba9-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="faba9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="faba9-108">EXAMPLES</span></span>

### <span data-ttu-id="faba9-109">Örnek 1: koruma varlığını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="faba9-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="faba9-110">İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak korumalı bir kapsayıcı alır ve bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="faba9-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="faba9-111">İkinci komut, **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanarak $Container depolanan kapsayıcıya ait korumalı sanal makineyi alır ve $ProtectionEntity değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="faba9-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="faba9-112">Son komut $ProtectionEntity koruma varlığını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="faba9-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="faba9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="faba9-113">PARAMETERS</span></span>

### <span data-ttu-id="faba9-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="faba9-114">-Profile</span></span>
<span data-ttu-id="faba9-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faba9-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="faba9-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="faba9-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="faba9-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="faba9-117">-ProtectionEntity</span></span>
<span data-ttu-id="faba9-118">Güncelleştirilecek bir koruma varlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="faba9-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="faba9-119">Bir **Asrprotectionentity** nesnesi almak için **Get-AzureSiteRecoveryProtectionEntity** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="faba9-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faba9-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="faba9-120">-WaitForCompletion</span></span>
<span data-ttu-id="faba9-121">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="faba9-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faba9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faba9-122">CommonParameters</span></span>
<span data-ttu-id="faba9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="faba9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faba9-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faba9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faba9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="faba9-125">INPUTS</span></span>

## <span data-ttu-id="faba9-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="faba9-126">OUTPUTS</span></span>

## <span data-ttu-id="faba9-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="faba9-127">NOTES</span></span>

## <span data-ttu-id="faba9-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="faba9-128">RELATED LINKS</span></span>

[<span data-ttu-id="faba9-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="faba9-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="faba9-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="faba9-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="faba9-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="faba9-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


