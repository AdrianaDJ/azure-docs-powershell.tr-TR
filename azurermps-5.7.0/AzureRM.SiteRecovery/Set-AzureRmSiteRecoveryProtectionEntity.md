---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762510"
---
# <span data-ttu-id="34760-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="34760-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="34760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34760-102">SYNOPSIS</span></span>
<span data-ttu-id="34760-103">Site kurtarma koruma varlığının durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34760-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34760-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34760-104">SYNTAX</span></span>

### <span data-ttu-id="34760-105">DisableDR (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34760-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34760-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="34760-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34760-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="34760-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34760-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="34760-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34760-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="34760-109">DESCRIPTION</span></span>
<span data-ttu-id="34760-110">**Set-AzureRmSiteRecoveryProtectionEntity** cmdlet 'ı bir Azure Site Recovery koruma varlığında korumayı devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="34760-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="34760-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34760-111">EXAMPLES</span></span>

## <span data-ttu-id="34760-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34760-112">PARAMETERS</span></span>

### <span data-ttu-id="34760-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34760-113">-DefaultProfile</span></span>
<span data-ttu-id="34760-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34760-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34760-115">-Force</span><span class="sxs-lookup"><span data-stu-id="34760-115">-Force</span></span>
<span data-ttu-id="34760-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="34760-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-117">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="34760-117">-OS</span></span>
<span data-ttu-id="34760-118">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="34760-118">Specifies the operating system type.</span></span>
<span data-ttu-id="34760-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="34760-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34760-120">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="34760-120">Windows</span></span>
- <span data-ttu-id="34760-121">UX</span><span class="sxs-lookup"><span data-stu-id="34760-121">Linux</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="34760-122">-OSDiskName</span></span>
<span data-ttu-id="34760-123">İşletim sistemini içeren diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34760-123">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-124">-İlke</span><span class="sxs-lookup"><span data-stu-id="34760-124">-Policy</span></span>
<span data-ttu-id="34760-125">Site kurtarma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34760-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-126">-Koruma</span><span class="sxs-lookup"><span data-stu-id="34760-126">-Protection</span></span>
<span data-ttu-id="34760-127">Korumanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34760-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="34760-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="34760-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34760-129">Etkinleştiremez</span><span class="sxs-lookup"><span data-stu-id="34760-129">Enable</span></span>
- <span data-ttu-id="34760-130">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="34760-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="34760-131">-ProtectionEntity</span></span>
<span data-ttu-id="34760-132">Koruma varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34760-132">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34760-133">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="34760-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="34760-134">Hedef Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="34760-134">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="34760-135">-WaitForCompletion</span></span>
<span data-ttu-id="34760-136">Komutun, dönmeden önce tamamlanması için beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="34760-136">Indicates that the command waits for completion before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="34760-137">-Confirm</span></span>
<span data-ttu-id="34760-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34760-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34760-139">-WhatIf</span></span>
<span data-ttu-id="34760-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34760-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="34760-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34760-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34760-142">CommonParameters</span></span>
<span data-ttu-id="34760-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34760-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34760-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34760-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34760-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34760-145">INPUTS</span></span>

### <span data-ttu-id="34760-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="34760-146">ASRProtectionEntity</span></span>
<span data-ttu-id="34760-147">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="34760-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="34760-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34760-148">OUTPUTS</span></span>

### <span data-ttu-id="34760-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="34760-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="34760-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34760-150">NOTES</span></span>

## <span data-ttu-id="34760-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34760-151">RELATED LINKS</span></span>

[<span data-ttu-id="34760-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="34760-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
