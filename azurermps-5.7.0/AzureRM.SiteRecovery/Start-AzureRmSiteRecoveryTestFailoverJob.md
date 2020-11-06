---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587423"
---
# <span data-ttu-id="25179-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="25179-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="25179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25179-102">SYNOPSIS</span></span>
<span data-ttu-id="25179-103">Site kurtarma koruma varlığı için test yük devretmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="25179-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25179-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25179-104">SYNTAX</span></span>

### <span data-ttu-id="25179-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25179-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="25179-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="25179-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="25179-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-109">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="25179-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="25179-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="25179-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="25179-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25179-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="25179-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25179-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="25179-114">DESCRIPTION</span></span>
<span data-ttu-id="25179-115">**Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet 'ı bir Azure Site Recovery koruma varlığının veya kurtarma planının yük devretmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="25179-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="25179-116">Get-AzureRmSiteRecoveryJob cmdlet 'ini kullanarak işin başarılı olup olmadığını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25179-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="25179-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25179-117">EXAMPLES</span></span>

## <span data-ttu-id="25179-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25179-118">PARAMETERS</span></span>

### <span data-ttu-id="25179-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="25179-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="25179-120">Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="25179-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25179-121">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="25179-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="25179-122">Birincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25179-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="25179-123">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="25179-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="25179-124">İkincil sertifika dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25179-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="25179-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25179-125">-DefaultProfile</span></span>
<span data-ttu-id="25179-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25179-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25179-127">-Yön</span><span class="sxs-lookup"><span data-stu-id="25179-127">-Direction</span></span>
<span data-ttu-id="25179-128">Yük devretme yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="25179-128">Specifies the failover direction.</span></span>
<span data-ttu-id="25179-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="25179-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25179-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="25179-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="25179-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="25179-131">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25179-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="25179-132">-ProtectionEntity</span></span>
<span data-ttu-id="25179-133">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25179-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25179-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="25179-134">-RecoveryPlan</span></span>
<span data-ttu-id="25179-135">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25179-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25179-136">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="25179-136">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25179-137">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="25179-137">-VMNetwork</span></span>
<span data-ttu-id="25179-138">Site kurtarma sanal makine ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25179-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25179-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25179-139">CommonParameters</span></span>
<span data-ttu-id="25179-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25179-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25179-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25179-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25179-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25179-142">INPUTS</span></span>

### <span data-ttu-id="25179-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="25179-143">ASRProtectionEntity</span></span>
<span data-ttu-id="25179-144">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="25179-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="25179-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="25179-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="25179-146">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="25179-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="25179-147">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="25179-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="25179-148">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="25179-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="25179-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25179-149">OUTPUTS</span></span>

### <span data-ttu-id="25179-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="25179-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="25179-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25179-151">NOTES</span></span>

## <span data-ttu-id="25179-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25179-152">RELATED LINKS</span></span>

[<span data-ttu-id="25179-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="25179-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
