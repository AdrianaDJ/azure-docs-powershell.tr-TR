---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762685"
---
# <span data-ttu-id="ebb7c-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="ebb7c-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="ebb7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb7c-103">Site kurtarma ile yönetilen sanal makineler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ebb7c-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebb7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebb7c-104">SYNTAX</span></span>

### <span data-ttu-id="ebb7c-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ebb7c-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb7c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ebb7c-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb7c-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ebb7c-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebb7c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebb7c-108">DESCRIPTION</span></span>
<span data-ttu-id="ebb7c-109">**Get-AzureRmSiteRecoveryVM** cmdlet 'ı Azure Site Recovery 'de yönetilen sanal makineler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ebb7c-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="ebb7c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebb7c-110">EXAMPLES</span></span>

## <span data-ttu-id="ebb7c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebb7c-111">PARAMETERS</span></span>

### <span data-ttu-id="ebb7c-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ebb7c-112">-FriendlyName</span></span>
<span data-ttu-id="ebb7c-113">Sanal makinenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebb7c-113">Specifies the friendly name of the virtual machine.</span></span>

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

### <span data-ttu-id="ebb7c-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="ebb7c-114">-Name</span></span>
<span data-ttu-id="ebb7c-115">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebb7c-115">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="ebb7c-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ebb7c-116">-ProtectionContainer</span></span>
<span data-ttu-id="ebb7c-117">Site Recovery koruması kapsayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebb7c-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb7c-118">-DefaultProfile</span></span>
<span data-ttu-id="ebb7c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ebb7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb7c-120">CommonParameters</span></span>
<span data-ttu-id="ebb7c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebb7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb7c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb7c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb7c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebb7c-123">INPUTS</span></span>

### <span data-ttu-id="ebb7c-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ebb7c-124">ASRProtectionContainer</span></span>
<span data-ttu-id="ebb7c-125">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ebb7c-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="ebb7c-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ebb7c-126">ASRProtectionContainer</span></span>
<span data-ttu-id="ebb7c-127">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ebb7c-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="ebb7c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebb7c-128">OUTPUTS</span></span>

### <span data-ttu-id="ebb7c-129">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="ebb7c-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="ebb7c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebb7c-130">NOTES</span></span>

## <span data-ttu-id="ebb7c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebb7c-131">RELATED LINKS</span></span>

[<span data-ttu-id="ebb7c-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="ebb7c-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
