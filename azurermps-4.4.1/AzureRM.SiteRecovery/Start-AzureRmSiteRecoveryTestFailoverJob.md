---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 330af3701741cbc83573afbbe7e283fdee294cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593784"
---
# <span data-ttu-id="0eccd-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0eccd-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="0eccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eccd-102">SYNOPSIS</span></span>
<span data-ttu-id="0eccd-103">Site kurtarma koruma varlığı için test yük devretmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0eccd-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eccd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0eccd-104">SYNTAX</span></span>

### <span data-ttu-id="0eccd-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0eccd-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0eccd-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0eccd-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0eccd-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-109">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="0eccd-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0eccd-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="0eccd-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0eccd-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eccd-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0eccd-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eccd-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="0eccd-114">DESCRIPTION</span></span>
<span data-ttu-id="0eccd-115">**Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet 'ı bir Azure Site Recovery koruma varlığının veya kurtarma planının yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0eccd-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="0eccd-116">Get-AzureRmSiteRecoveryJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0eccd-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="0eccd-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0eccd-117">EXAMPLES</span></span>

## <span data-ttu-id="0eccd-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0eccd-118">PARAMETERS</span></span>

### <span data-ttu-id="0eccd-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0eccd-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="0eccd-120">Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eccd-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccd-121">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="0eccd-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0eccd-122">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eccd-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="0eccd-123">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="0eccd-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0eccd-124">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eccd-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="0eccd-125">-Yön</span><span class="sxs-lookup"><span data-stu-id="0eccd-125">-Direction</span></span>
<span data-ttu-id="0eccd-126">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eccd-126">Specifies the failover direction.</span></span>
<span data-ttu-id="0eccd-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0eccd-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0eccd-128">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0eccd-128">PrimaryToRecovery</span></span>
- <span data-ttu-id="0eccd-129">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0eccd-129">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccd-130">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0eccd-130">-ProtectionEntity</span></span>
<span data-ttu-id="0eccd-131">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eccd-131">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccd-132">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0eccd-132">-RecoveryPlan</span></span>
<span data-ttu-id="0eccd-133">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eccd-133">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccd-134">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="0eccd-134">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eccd-135">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="0eccd-135">-VMNetwork</span></span>
<span data-ttu-id="0eccd-136">Site kurtarma sanal makine ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eccd-136">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eccd-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eccd-137">-DefaultProfile</span></span>
<span data-ttu-id="0eccd-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0eccd-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eccd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eccd-139">CommonParameters</span></span>
<span data-ttu-id="0eccd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0eccd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eccd-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eccd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eccd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0eccd-142">INPUTS</span></span>

### <span data-ttu-id="0eccd-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0eccd-143">ASRProtectionEntity</span></span>
<span data-ttu-id="0eccd-144">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0eccd-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="0eccd-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0eccd-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="0eccd-146">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0eccd-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="0eccd-147">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="0eccd-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="0eccd-148">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0eccd-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="0eccd-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0eccd-149">OUTPUTS</span></span>

### <span data-ttu-id="0eccd-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0eccd-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0eccd-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0eccd-151">NOTES</span></span>

## <span data-ttu-id="0eccd-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0eccd-152">RELATED LINKS</span></span>

[<span data-ttu-id="0eccd-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0eccd-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
