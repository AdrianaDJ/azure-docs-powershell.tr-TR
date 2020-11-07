---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 8df9d0b5149ef3b22477be1f2316bf499a3b1c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932664"
---
# <span data-ttu-id="f4c2f-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="f4c2f-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="f4c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c2f-103">Yalnızca sorun giderme için kullanın.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-103">Use for troubleshooting only.</span></span> <span data-ttu-id="f4c2f-104">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="f4c2f-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4c2f-105">SYNTAX</span></span>

### <span data-ttu-id="f4c2f-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4c2f-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c2f-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4c2f-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c2f-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4c2f-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c2f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4c2f-109">DESCRIPTION</span></span>
<span data-ttu-id="f4c2f-110">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="f4c2f-111">Bu, sorun giderme senaryolarında kullanılması amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="f4c2f-112">Bu komut çağrılırken, sunucu sertifikası değiştirilir, bu sunucunun ortak bölümü gönderilirken, bu sunucunun da birlikte kaydedildiği depolama eşitleme hizmeti güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="f4c2f-113">Yeni bir sertifika oluşturulduğundan bu sertifikanın son kullanma tarihi de güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="f4c2f-114">Bu komut, süresi dolan bir sertifikayı güncelleştirmek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="f4c2f-115">Bu durum, sunucu uzun süre çevrimdışı olduğunda oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="f4c2f-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4c2f-116">EXAMPLES</span></span>

### <span data-ttu-id="f4c2f-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4c2f-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="f4c2f-118">Bu komut, yerel sunucu sertifikasını alır ve sunucunun yeni kimliğinin ilgili depolama eşitleme hizmeti 'ni güvenli bir şekilde bilgilendirecektir.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="f4c2f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4c2f-119">PARAMETERS</span></span>

### <span data-ttu-id="f4c2f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c2f-120">-DefaultProfile</span></span>
<span data-ttu-id="f4c2f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c2f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4c2f-122">-ParentObject</span></span>
<span data-ttu-id="f4c2f-123">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c2f-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="f4c2f-124">-ParentResourceId</span></span>
<span data-ttu-id="f4c2f-125">StorageSyncService üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f4c2f-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c2f-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f4c2f-126">-PassThru</span></span>
<span data-ttu-id="f4c2f-127">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f4c2f-128">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f4c2f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c2f-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4c2f-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c2f-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f4c2f-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="f4c2f-132">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-132">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c2f-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4c2f-133">-Confirm</span></span>
<span data-ttu-id="f4c2f-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c2f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c2f-135">-WhatIf</span></span>
<span data-ttu-id="f4c2f-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c2f-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c2f-138">CommonParameters</span></span>
<span data-ttu-id="f4c2f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4c2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c2f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c2f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c2f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4c2f-141">INPUTS</span></span>

### <span data-ttu-id="f4c2f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f4c2f-142">System.String</span></span>

### <span data-ttu-id="f4c2f-143">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f4c2f-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f4c2f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4c2f-144">OUTPUTS</span></span>

### <span data-ttu-id="f4c2f-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="f4c2f-145">System.Object</span></span>
## <span data-ttu-id="f4c2f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4c2f-146">NOTES</span></span>

## <span data-ttu-id="f4c2f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4c2f-147">RELATED LINKS</span></span>
