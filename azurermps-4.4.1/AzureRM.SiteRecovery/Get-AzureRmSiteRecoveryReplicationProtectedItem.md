---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 0e94a46b8d6433ddd96530dc011234050398bf37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593789"
---
# <span data-ttu-id="6d767-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d767-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="6d767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d767-102">SYNOPSIS</span></span>
<span data-ttu-id="6d767-103">Azure Site Recovery korumalı öğelerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6d767-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d767-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d767-104">SYNTAX</span></span>

### <span data-ttu-id="6d767-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d767-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d767-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6d767-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d767-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6d767-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d767-108">Bykorunabilir ıtemobject</span><span class="sxs-lookup"><span data-stu-id="6d767-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d767-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d767-109">DESCRIPTION</span></span>
<span data-ttu-id="6d767-110">**Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet 'ı, Azure Site Recovery korumalı öğelerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6d767-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="6d767-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d767-111">EXAMPLES</span></span>

## <span data-ttu-id="6d767-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d767-112">PARAMETERS</span></span>

### <span data-ttu-id="6d767-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6d767-113">-FriendlyName</span></span>
<span data-ttu-id="6d767-114">Bu cmdlet 'in aldığı çoğaltma korumalı öğesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d767-114">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d767-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d767-115">-Name</span></span>
<span data-ttu-id="6d767-116">Bu cmdlet 'in aldığı çoğaltma korumalı öğesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d767-116">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d767-117">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="6d767-117">-ProtectableItem</span></span>
<span data-ttu-id="6d767-118">Çoğaltma korumalı öğeye karşılık gelen korunabilir öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d767-118">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d767-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6d767-119">-ProtectionContainer</span></span>
<span data-ttu-id="6d767-120">Azure Site Recovery koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d767-120">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d767-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d767-121">-DefaultProfile</span></span>
<span data-ttu-id="6d767-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d767-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d767-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d767-123">CommonParameters</span></span>
<span data-ttu-id="6d767-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d767-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d767-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d767-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d767-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d767-126">INPUTS</span></span>

### <span data-ttu-id="6d767-127">Asrkorunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="6d767-127">ASRProtectableItem</span></span>
<span data-ttu-id="6d767-128">Parametre ' korunabilir öğe ', ardışık düzenin ' Asrkorunabilir öğe ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6d767-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="6d767-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6d767-129">ASRProtectionContainer</span></span>
<span data-ttu-id="6d767-130">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6d767-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="6d767-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d767-131">OUTPUTS</span></span>

### <span data-ttu-id="6d767-132">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. Asrreplicationkorunabilir 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6d767-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6d767-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d767-133">NOTES</span></span>

## <span data-ttu-id="6d767-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d767-134">RELATED LINKS</span></span>

[<span data-ttu-id="6d767-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d767-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="6d767-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d767-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="6d767-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6d767-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
