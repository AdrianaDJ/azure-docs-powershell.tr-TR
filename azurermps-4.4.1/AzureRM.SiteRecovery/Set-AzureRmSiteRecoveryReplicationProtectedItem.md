---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589069"
---
# <span data-ttu-id="cf996-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf996-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="cf996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf996-102">SYNOPSIS</span></span>
<span data-ttu-id="cf996-103">Çoğaltma korumalı öğenin hedef ağ ve sanal makine boyutu gibi kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf996-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf996-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf996-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf996-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf996-105">DESCRIPTION</span></span>
<span data-ttu-id="cf996-106">**Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet 'ı, çoğaltma korumalı öğenin kurtarma özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf996-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="cf996-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf996-107">EXAMPLES</span></span>

## <span data-ttu-id="cf996-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf996-108">PARAMETERS</span></span>

### <span data-ttu-id="cf996-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cf996-109">-LicenseType</span></span>
<span data-ttu-id="cf996-110">Karma kullanım avantajı aracılığıyla geçirilen Windows Server sanal makinelerinin lisans türü seçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf996-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf996-111">-Name</span></span>
<span data-ttu-id="cf996-112">Kurtarma sanal makinesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-112">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="cf996-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="cf996-113">-NicSelectionType</span></span>
<span data-ttu-id="cf996-114">Kullanıcı tarafından ayarlanan ağ arabirim kartı (NIC) özelliklerini belirtir veya varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="cf996-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="cf996-115">Varsayılan değerlere dönmek için NotSelected belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf996-115">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="cf996-116">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="cf996-116">-PrimaryNic</span></span>
<span data-ttu-id="cf996-117">Bu cmdlet 'in kurtarma ağı özelliğini ayarladığı sanal makinenin NIC 'ini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="cf996-118">-Recoverynetworkıd</span><span class="sxs-lookup"><span data-stu-id="cf996-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="cf996-119">Bu cmdlet 'in korumalı öğeyi kurtaramadığı Azure sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="cf996-120">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="cf996-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="cf996-121">Kurtarmada birincil NIC 'ye atanması gereken statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="cf996-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="cf996-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="cf996-123">Bu cmdlet 'in korumalı öğeyi kurtaramadığı, kurtarma Azure sanal ağında alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="cf996-124">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="cf996-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cf996-125">Azure Site Recovery çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf996-126">-Boyut</span><span class="sxs-lookup"><span data-stu-id="cf996-126">-Size</span></span>
<span data-ttu-id="cf996-127">Kurtarma sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf996-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="cf996-128">Değer, Azure sanal makinelerinin desteklediği boyutlar kümesinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf996-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="cf996-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf996-129">-DefaultProfile</span></span>
<span data-ttu-id="cf996-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf996-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf996-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf996-131">CommonParameters</span></span>
<span data-ttu-id="cf996-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf996-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf996-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf996-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf996-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf996-134">INPUTS</span></span>

### <span data-ttu-id="cf996-135">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="cf996-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="cf996-136">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cf996-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="cf996-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf996-137">OUTPUTS</span></span>

### <span data-ttu-id="cf996-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cf996-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cf996-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf996-139">NOTES</span></span>

## <span data-ttu-id="cf996-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf996-140">RELATED LINKS</span></span>

[<span data-ttu-id="cf996-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf996-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="cf996-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf996-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="cf996-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cf996-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
