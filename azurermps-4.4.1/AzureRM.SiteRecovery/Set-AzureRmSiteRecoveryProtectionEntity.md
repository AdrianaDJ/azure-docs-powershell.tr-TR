---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763309"
---
# <span data-ttu-id="5d8d1-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5d8d1-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="5d8d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8d1-103">Site kurtarma koruma varlığının durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d8d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d8d1-104">SYNTAX</span></span>

### <span data-ttu-id="5d8d1-105">DisableDR (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d8d1-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d8d1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5d8d1-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8d1-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5d8d1-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8d1-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="5d8d1-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d8d1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d8d1-109">DESCRIPTION</span></span>
<span data-ttu-id="5d8d1-110">**Set-AzureRmSiteRecoveryProtectionEntity** cmdlet 'ı bir Azure Site Recovery koruma varlığında korumayı devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="5d8d1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d8d1-111">EXAMPLES</span></span>

## <span data-ttu-id="5d8d1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d8d1-112">PARAMETERS</span></span>

### <span data-ttu-id="5d8d1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5d8d1-113">-Force</span></span>
<span data-ttu-id="5d8d1-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-115">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="5d8d1-115">-OS</span></span>
<span data-ttu-id="5d8d1-116">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-116">Specifies the operating system type.</span></span>
<span data-ttu-id="5d8d1-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5d8d1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d8d1-118">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="5d8d1-118">Windows</span></span>
- <span data-ttu-id="5d8d1-119">UX</span><span class="sxs-lookup"><span data-stu-id="5d8d1-119">Linux</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="5d8d1-120">-OSDiskName</span></span>
<span data-ttu-id="5d8d1-121">İşletim sistemini içeren diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-121">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-122">-İlke</span><span class="sxs-lookup"><span data-stu-id="5d8d1-122">-Policy</span></span>
<span data-ttu-id="5d8d1-123">Site kurtarma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-124">-Koruma</span><span class="sxs-lookup"><span data-stu-id="5d8d1-124">-Protection</span></span>
<span data-ttu-id="5d8d1-125">Korumanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="5d8d1-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5d8d1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d8d1-127">Etkinleştiremez</span><span class="sxs-lookup"><span data-stu-id="5d8d1-127">Enable</span></span>
- <span data-ttu-id="5d8d1-128">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="5d8d1-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5d8d1-129">-ProtectionEntity</span></span>
<span data-ttu-id="5d8d1-130">Koruma varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-131">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5d8d1-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="5d8d1-132">Hedef Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-132">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5d8d1-133">-WaitForCompletion</span></span>
<span data-ttu-id="5d8d1-134">Komutun, dönmeden önce tamamlanması için beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-134">Indicates that the command waits for completion before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="5d8d1-135">-Confirm</span></span>
<span data-ttu-id="5d8d1-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d8d1-137">-WhatIf</span></span>
<span data-ttu-id="5d8d1-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5d8d1-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8d1-140">-DefaultProfile</span></span>
<span data-ttu-id="5d8d1-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d8d1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8d1-142">CommonParameters</span></span>
<span data-ttu-id="5d8d1-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d8d1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8d1-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d8d1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8d1-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d8d1-145">INPUTS</span></span>

### <span data-ttu-id="5d8d1-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5d8d1-146">ASRProtectionEntity</span></span>
<span data-ttu-id="5d8d1-147">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5d8d1-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="5d8d1-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d8d1-148">OUTPUTS</span></span>

### <span data-ttu-id="5d8d1-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5d8d1-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5d8d1-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d8d1-150">NOTES</span></span>

## <span data-ttu-id="5d8d1-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d8d1-151">RELATED LINKS</span></span>

[<span data-ttu-id="5d8d1-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5d8d1-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)