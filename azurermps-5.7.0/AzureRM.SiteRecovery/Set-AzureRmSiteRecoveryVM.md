---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: b330cb59281a3f140ba30f10f31ecb5bf3b49f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593375"
---
# <span data-ttu-id="87f6d-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="87f6d-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="87f6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="87f6d-103">Site kurtarma koruma varlığının kurtarma tarafı seçeneklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87f6d-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87f6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87f6d-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87f6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="87f6d-106">**Set-AzureRmSiteRecoveryVM** cmdlet 'ı, Azure Site Recovery koruma varlıkları için kurtarma sanal makine boyutu ve kurtarma sanal makine ağı gibi kurtarma tarafı koruma seçeneklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87f6d-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="87f6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87f6d-107">EXAMPLES</span></span>

## <span data-ttu-id="87f6d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87f6d-108">PARAMETERS</span></span>

### <span data-ttu-id="87f6d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f6d-109">-DefaultProfile</span></span>
<span data-ttu-id="87f6d-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87f6d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87f6d-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="87f6d-111">-Name</span></span>
<span data-ttu-id="87f6d-112">Hedef sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-112">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="87f6d-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="87f6d-113">-NicSelectionType</span></span>
<span data-ttu-id="87f6d-114">Ağ bağdaştırıcısı seçim özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-114">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="87f6d-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="87f6d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87f6d-116">NotSelected</span><span class="sxs-lookup"><span data-stu-id="87f6d-116">NotSelected</span></span>
- <span data-ttu-id="87f6d-117">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="87f6d-117">SelectedByUser</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f6d-118">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="87f6d-118">-PrimaryNic</span></span>
<span data-ttu-id="87f6d-119">Birincil ağ bağdaştırıcı kartını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-119">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="87f6d-120">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="87f6d-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="87f6d-121">Kurtarma ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-121">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="87f6d-122">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="87f6d-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="87f6d-123">Kurtarma sırasında birincil ağ bağdaştırıcısı denetleyicisine atanan statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-123">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="87f6d-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="87f6d-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="87f6d-125">Kurtarma sırasında birincil ağ bağdaştırıcısı denetleyicisinin ekleneceği Azure sanal ağ alt ağı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-125">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="87f6d-126">-Boyut</span><span class="sxs-lookup"><span data-stu-id="87f6d-126">-Size</span></span>
<span data-ttu-id="87f6d-127">Hedef sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-127">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="87f6d-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="87f6d-128">-VirtualMachine</span></span>
<span data-ttu-id="87f6d-129">Site kurtarma sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f6d-129">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87f6d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f6d-130">CommonParameters</span></span>
<span data-ttu-id="87f6d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87f6d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f6d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f6d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f6d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87f6d-133">INPUTS</span></span>

### <span data-ttu-id="87f6d-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="87f6d-134">ASRVirtualMachine</span></span>
<span data-ttu-id="87f6d-135">Parametre ' VirtualMachine ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="87f6d-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="87f6d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87f6d-136">OUTPUTS</span></span>

### <span data-ttu-id="87f6d-137">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="87f6d-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="87f6d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87f6d-138">NOTES</span></span>

## <span data-ttu-id="87f6d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87f6d-139">RELATED LINKS</span></span>

[<span data-ttu-id="87f6d-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="87f6d-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
