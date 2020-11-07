---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753950"
---
# <span data-ttu-id="91147-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="91147-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="91147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91147-102">SYNOPSIS</span></span>
<span data-ttu-id="91147-103">Yalnızca sorun giderme için kullanın.</span><span class="sxs-lookup"><span data-stu-id="91147-103">Use for troubleshooting only.</span></span> <span data-ttu-id="91147-104">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="91147-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="91147-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91147-105">SYNTAX</span></span>

### <span data-ttu-id="91147-106">ObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91147-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91147-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="91147-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91147-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="91147-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91147-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="91147-109">DESCRIPTION</span></span>
<span data-ttu-id="91147-110">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="91147-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="91147-111">Bu, sorun giderme senaryolarında kullanılması amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="91147-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="91147-112">Bu komut çağrılırken, sunucu sertifikası değiştirilir, bu sunucunun ortak bölümü gönderilirken, bu sunucunun da birlikte kaydedildiği depolama eşitleme hizmeti güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="91147-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="91147-113">Yeni bir sertifika oluşturulduğundan bu sertifikanın son kullanma tarihi de güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="91147-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="91147-114">Bu komut, süresi dolan bir sertifikayı güncelleştirmek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="91147-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="91147-115">Bu durum, sunucu uzun süre çevrimdışı olduğunda oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="91147-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="91147-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91147-116">EXAMPLES</span></span>

### <span data-ttu-id="91147-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91147-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="91147-118">Bu komut, yerel sunucu sertifikasını alır ve sunucunun yeni kimliğinin ilgili depolama eşitleme hizmeti 'ni güvenli bir şekilde bilgilendirecektir.</span><span class="sxs-lookup"><span data-stu-id="91147-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="91147-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91147-119">PARAMETERS</span></span>

### <span data-ttu-id="91147-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91147-120">-DefaultProfile</span></span>
<span data-ttu-id="91147-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91147-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91147-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="91147-122">-ParentObject</span></span>
<span data-ttu-id="91147-123">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="91147-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="91147-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="91147-124">-ParentResourceId</span></span>
<span data-ttu-id="91147-125">StorageSyncService üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="91147-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="91147-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="91147-126">-PassThru</span></span>
<span data-ttu-id="91147-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="91147-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="91147-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91147-128">-ResourceGroupName</span></span>
<span data-ttu-id="91147-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="91147-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="91147-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="91147-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="91147-131">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="91147-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="91147-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="91147-132">-Confirm</span></span>
<span data-ttu-id="91147-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91147-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91147-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91147-134">-WhatIf</span></span>
<span data-ttu-id="91147-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91147-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91147-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91147-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91147-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91147-137">CommonParameters</span></span>
<span data-ttu-id="91147-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91147-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91147-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91147-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91147-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91147-140">INPUTS</span></span>

### <span data-ttu-id="91147-141">System. String</span><span class="sxs-lookup"><span data-stu-id="91147-141">System.String</span></span>

### <span data-ttu-id="91147-142">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="91147-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="91147-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91147-143">OUTPUTS</span></span>

### <span data-ttu-id="91147-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="91147-144">System.Object</span></span>
## <span data-ttu-id="91147-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91147-145">NOTES</span></span>

## <span data-ttu-id="91147-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91147-146">RELATED LINKS</span></span>
