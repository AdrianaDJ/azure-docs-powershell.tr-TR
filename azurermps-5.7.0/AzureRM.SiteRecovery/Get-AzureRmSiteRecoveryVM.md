---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593394"
---
# <span data-ttu-id="3e063-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3e063-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="3e063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e063-102">SYNOPSIS</span></span>
<span data-ttu-id="3e063-103">Site kurtarma ile yönetilen sanal makineler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3e063-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e063-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e063-104">SYNTAX</span></span>

### <span data-ttu-id="3e063-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e063-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e063-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3e063-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e063-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3e063-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e063-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e063-108">DESCRIPTION</span></span>
<span data-ttu-id="3e063-109">**Get-AzureRmSiteRecoveryVM** cmdlet 'ı Azure Site Recovery 'de yönetilen sanal makineler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3e063-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="3e063-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e063-110">EXAMPLES</span></span>

## <span data-ttu-id="3e063-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e063-111">PARAMETERS</span></span>

### <span data-ttu-id="3e063-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e063-112">-DefaultProfile</span></span>
<span data-ttu-id="3e063-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e063-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e063-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3e063-114">-FriendlyName</span></span>
<span data-ttu-id="3e063-115">Sanal makinenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e063-115">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e063-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e063-116">-Name</span></span>
<span data-ttu-id="3e063-117">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e063-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e063-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3e063-118">-ProtectionContainer</span></span>
<span data-ttu-id="3e063-119">Site Recovery koruması kapsayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e063-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e063-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e063-120">CommonParameters</span></span>
<span data-ttu-id="3e063-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e063-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e063-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e063-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e063-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e063-123">INPUTS</span></span>

### <span data-ttu-id="3e063-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3e063-124">ASRProtectionContainer</span></span>
<span data-ttu-id="3e063-125">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3e063-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="3e063-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3e063-126">ASRProtectionContainer</span></span>
<span data-ttu-id="3e063-127">' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3e063-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="3e063-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e063-128">OUTPUTS</span></span>

### <span data-ttu-id="3e063-129">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="3e063-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="3e063-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e063-130">NOTES</span></span>

## <span data-ttu-id="3e063-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e063-131">RELATED LINKS</span></span>

[<span data-ttu-id="3e063-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3e063-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
