---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 41caebb8b43c7c050aef2dac77daf51eebdaf42a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273781"
---
# <span data-ttu-id="6578a-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="6578a-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="6578a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6578a-102">SYNOPSIS</span></span>
<span data-ttu-id="6578a-103">Yalnızca sorun giderme için kullanın.</span><span class="sxs-lookup"><span data-stu-id="6578a-103">Use for troubleshooting only.</span></span> <span data-ttu-id="6578a-104">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="6578a-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="6578a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6578a-105">SYNTAX</span></span>

### <span data-ttu-id="6578a-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6578a-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6578a-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6578a-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6578a-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6578a-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6578a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6578a-109">DESCRIPTION</span></span>
<span data-ttu-id="6578a-110">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="6578a-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="6578a-111">Bu, sorun giderme senaryolarında kullanılması amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6578a-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="6578a-112">Bu komut çağrılırken, sunucu sertifikası değiştirilir, bu sunucunun ortak bölümü gönderilirken, bu sunucunun da birlikte kaydedildiği depolama eşitleme hizmeti güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6578a-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="6578a-113">Yeni bir sertifika oluşturulduğundan bu sertifikanın son kullanma tarihi de güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6578a-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="6578a-114">Bu komut, süresi dolan bir sertifikayı güncelleştirmek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6578a-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="6578a-115">Bu durum, sunucu uzun süre çevrimdışı olduğunda oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="6578a-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="6578a-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6578a-116">EXAMPLES</span></span>

### <span data-ttu-id="6578a-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6578a-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="6578a-118">Bu komut, yerel sunucu sertifikasını alır ve sunucunun yeni kimliğinin ilgili depolama eşitleme hizmeti 'ni güvenli bir şekilde bilgilendirecektir.</span><span class="sxs-lookup"><span data-stu-id="6578a-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="6578a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6578a-119">PARAMETERS</span></span>

### <span data-ttu-id="6578a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6578a-120">-DefaultProfile</span></span>
<span data-ttu-id="6578a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6578a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6578a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6578a-122">-ParentObject</span></span>
<span data-ttu-id="6578a-123">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6578a-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="6578a-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="6578a-124">-ParentResourceId</span></span>
<span data-ttu-id="6578a-125">StorageSyncService üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6578a-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="6578a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6578a-126">-PassThru</span></span>
<span data-ttu-id="6578a-127">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="6578a-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="6578a-128">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="6578a-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="6578a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6578a-129">-ResourceGroupName</span></span>
<span data-ttu-id="6578a-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6578a-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="6578a-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6578a-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="6578a-132">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="6578a-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6578a-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="6578a-133">-Confirm</span></span>
<span data-ttu-id="6578a-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6578a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6578a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6578a-135">-WhatIf</span></span>
<span data-ttu-id="6578a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6578a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6578a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6578a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6578a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6578a-138">CommonParameters</span></span>
<span data-ttu-id="6578a-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6578a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6578a-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6578a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6578a-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6578a-141">INPUTS</span></span>

### <span data-ttu-id="6578a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6578a-142">System.String</span></span>

### <span data-ttu-id="6578a-143">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="6578a-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="6578a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6578a-144">OUTPUTS</span></span>

### <span data-ttu-id="6578a-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="6578a-145">System.Object</span></span>
## <span data-ttu-id="6578a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6578a-146">NOTES</span></span>

## <span data-ttu-id="6578a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6578a-147">RELATED LINKS</span></span>
