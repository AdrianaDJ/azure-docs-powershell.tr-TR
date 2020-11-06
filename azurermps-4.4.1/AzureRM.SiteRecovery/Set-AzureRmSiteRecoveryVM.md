---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 7cfc764e5c9c3c5bb11290220cc04b2baa781070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592538"
---
# <span data-ttu-id="5c800-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="5c800-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="5c800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c800-102">SYNOPSIS</span></span>
<span data-ttu-id="5c800-103">Site kurtarma koruma varlığının kurtarma tarafı seçeneklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c800-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c800-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c800-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c800-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c800-105">DESCRIPTION</span></span>
<span data-ttu-id="5c800-106">**Set-AzureRmSiteRecoveryVM** cmdlet 'ı, Azure Site Recovery koruma varlıkları için kurtarma sanal makine boyutu ve kurtarma sanal makine ağı gibi kurtarma tarafı koruma seçeneklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c800-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="5c800-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c800-107">EXAMPLES</span></span>

## <span data-ttu-id="5c800-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c800-108">PARAMETERS</span></span>

### <span data-ttu-id="5c800-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c800-109">-Name</span></span>
<span data-ttu-id="5c800-110">Hedef sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-110">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-111">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="5c800-111">-NicSelectionType</span></span>
<span data-ttu-id="5c800-112">Ağ bağdaştırıcısı seçim özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-112">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="5c800-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5c800-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c800-114">NotSelected</span><span class="sxs-lookup"><span data-stu-id="5c800-114">NotSelected</span></span>
- <span data-ttu-id="5c800-115">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="5c800-115">SelectedByUser</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-116">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="5c800-116">-PrimaryNic</span></span>
<span data-ttu-id="5c800-117">Birincil ağ bağdaştırıcı kartını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-117">Specifies the primary network adapter card.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-118">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="5c800-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="5c800-119">Kurtarma ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-119">Specifies the recovery network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-120">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="5c800-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="5c800-121">Kurtarma sırasında birincil ağ bağdaştırıcısı denetleyicisine atanan statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-121">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="5c800-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="5c800-123">Kurtarma sırasında birincil ağ bağdaştırıcısı denetleyicisinin ekleneceği Azure sanal ağ alt ağı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-123">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-124">-Boyut</span><span class="sxs-lookup"><span data-stu-id="5c800-124">-Size</span></span>
<span data-ttu-id="5c800-125">Hedef sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-125">Specifies the target virtual machine size.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-126">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5c800-126">-VirtualMachine</span></span>
<span data-ttu-id="5c800-127">Site kurtarma sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c800-127">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c800-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c800-128">-DefaultProfile</span></span>
<span data-ttu-id="5c800-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c800-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c800-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c800-130">CommonParameters</span></span>
<span data-ttu-id="5c800-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c800-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c800-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c800-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c800-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c800-133">INPUTS</span></span>

### <span data-ttu-id="5c800-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5c800-134">ASRVirtualMachine</span></span>
<span data-ttu-id="5c800-135">Parametre ' VirtualMachine ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="5c800-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="5c800-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c800-136">OUTPUTS</span></span>

### <span data-ttu-id="5c800-137">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c800-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c800-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c800-138">NOTES</span></span>

## <span data-ttu-id="5c800-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c800-139">RELATED LINKS</span></span>

[<span data-ttu-id="5c800-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="5c800-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
