---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: fa308c0961d11320964d7c31a7d77642e968b09b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763317"
---
# <span data-ttu-id="b5f44-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5f44-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="b5f44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f44-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f44-103">Site kurtarma 'da site kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5f44-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5f44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5f44-104">SYNTAX</span></span>

### <span data-ttu-id="b5f44-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5f44-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5f44-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b5f44-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5f44-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="b5f44-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5f44-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="b5f44-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5f44-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="b5f44-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5f44-110">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="b5f44-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5f44-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5f44-111">DESCRIPTION</span></span>
<span data-ttu-id="b5f44-112">**New-AzureRmSiteRecoveryRecoveryPlan** cmdlet 'ı Azure Site Recovery 'de bir kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5f44-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="b5f44-113">Kurtarma planı bir gruptaki sanal makineleri, yük devretme ve kurtarma amacıyla alır.</span><span class="sxs-lookup"><span data-stu-id="b5f44-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="b5f44-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5f44-114">EXAMPLES</span></span>

### <span data-ttu-id="b5f44-115">Örnek 1: site kurtarma kasasına kurtarma planı ekleme</span><span class="sxs-lookup"><span data-stu-id="b5f44-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="b5f44-116">Bu komut RecoveryPlan.xml adlı kurtarma planını Azure Site Recovery kasasına ekler.</span><span class="sxs-lookup"><span data-stu-id="b5f44-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b5f44-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5f44-117">PARAMETERS</span></span>

### <span data-ttu-id="b5f44-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="b5f44-118">-Azure</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="b5f44-119">-FailoverDeploymentModel</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5f44-120">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-121">-Yol</span><span class="sxs-lookup"><span data-stu-id="b5f44-121">-Path</span></span>
<span data-ttu-id="b5f44-122">Kurtarma planı dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5f44-122">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-123">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="b5f44-123">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-124">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="b5f44-124">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-125">-Primarysıte</span><span class="sxs-lookup"><span data-stu-id="b5f44-125">-PrimarySite</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-126">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="b5f44-126">-ProtectionEntityList</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-127">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b5f44-127">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-128">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b5f44-128">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-129">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="b5f44-129">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f44-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f44-130">-DefaultProfile</span></span>
<span data-ttu-id="b5f44-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5f44-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5f44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f44-132">CommonParameters</span></span>
<span data-ttu-id="b5f44-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5f44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f44-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f44-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f44-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5f44-135">INPUTS</span></span>

### <span data-ttu-id="b5f44-136">ASRProtectionEntity []</span><span class="sxs-lookup"><span data-stu-id="b5f44-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="b5f44-137">' ProtectionEntityList ' parametresi ardışık düzene ' ASRProtectionEntity [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b5f44-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="b5f44-138">Asrreplicationkorunabilir []</span><span class="sxs-lookup"><span data-stu-id="b5f44-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="b5f44-139">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="b5f44-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="b5f44-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5f44-140">OUTPUTS</span></span>

## <span data-ttu-id="b5f44-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5f44-141">NOTES</span></span>

## <span data-ttu-id="b5f44-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5f44-142">RELATED LINKS</span></span>

[<span data-ttu-id="b5f44-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5f44-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b5f44-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5f44-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b5f44-145">Güncelleştirme-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b5f44-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)

