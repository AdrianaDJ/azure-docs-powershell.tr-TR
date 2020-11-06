---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e09cc216b7ba3ef383467ea53478cfe8819e0a4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593377"
---
# <span data-ttu-id="c026c-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c026c-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="c026c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c026c-102">SYNOPSIS</span></span>
<span data-ttu-id="c026c-103">Çoğaltma korumalı öğenin hedef ağ ve sanal makine boyutu gibi kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c026c-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c026c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c026c-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c026c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c026c-105">DESCRIPTION</span></span>
<span data-ttu-id="c026c-106">**Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet 'ı, çoğaltma korumalı öğenin kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c026c-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="c026c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c026c-107">EXAMPLES</span></span>

## <span data-ttu-id="c026c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c026c-108">PARAMETERS</span></span>

### <span data-ttu-id="c026c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c026c-109">-DefaultProfile</span></span>
<span data-ttu-id="c026c-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c026c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c026c-111">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c026c-111">-LicenseType</span></span>
<span data-ttu-id="c026c-112">Karma kullanım avantajı aracılığıyla geçirilen Windows Server sanal makinelerinin lisans türü seçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-112">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c026c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c026c-113">-Name</span></span>
<span data-ttu-id="c026c-114">Kurtarma sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-114">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="c026c-115">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="c026c-115">-NicSelectionType</span></span>
<span data-ttu-id="c026c-116">Kullanıcı tarafından ayarlanan ağ arabirim kartı (NIC) özelliklerini belirtir veya varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c026c-116">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="c026c-117">Varsayılan değerlere dönmek için NotSelected belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c026c-117">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="c026c-118">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="c026c-118">-PrimaryNic</span></span>
<span data-ttu-id="c026c-119">Bu cmdlet 'in kurtarma ağı özelliğini ayarladığı sanal makinenin NIC 'ini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-119">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="c026c-120">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="c026c-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="c026c-121">Bu cmdlet 'in korumalı öğeyi kurtaramadığı Azure sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-121">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="c026c-122">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="c026c-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="c026c-123">Kurtarmada birincil NIC 'ye atanması gereken statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-123">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="c026c-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c026c-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="c026c-125">Bu cmdlet 'in korumalı öğeyi kurtaramadığı, kurtarma Azure sanal ağında alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-125">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="c026c-126">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="c026c-126">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c026c-127">Azure Site Recovery çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-127">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c026c-128">-Boyut</span><span class="sxs-lookup"><span data-stu-id="c026c-128">-Size</span></span>
<span data-ttu-id="c026c-129">Kurtarma sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c026c-129">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="c026c-130">Değer, Azure sanal makinelerinin desteklediği boyutlar kümesinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c026c-130">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="c026c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c026c-131">CommonParameters</span></span>
<span data-ttu-id="c026c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c026c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c026c-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c026c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c026c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c026c-134">INPUTS</span></span>

### <span data-ttu-id="c026c-135">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="c026c-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="c026c-136">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c026c-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="c026c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c026c-137">OUTPUTS</span></span>

### <span data-ttu-id="c026c-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c026c-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c026c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c026c-139">NOTES</span></span>

## <span data-ttu-id="c026c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c026c-140">RELATED LINKS</span></span>

[<span data-ttu-id="c026c-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c026c-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c026c-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c026c-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c026c-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c026c-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
