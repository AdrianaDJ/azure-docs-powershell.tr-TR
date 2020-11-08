---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098653"
---
# <span data-ttu-id="f4e3a-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f4e3a-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="f4e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e3a-103">Bu komut, belirtilen depolama eşitleme hizmeti 'ni silecek.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="f4e3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4e3a-104">SYNTAX</span></span>

### <span data-ttu-id="f4e3a-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4e3a-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e3a-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="f4e3a-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e3a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f4e3a-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e3a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4e3a-108">DESCRIPTION</span></span>
<span data-ttu-id="f4e3a-109">Bu komut, belirtilen depolama eşitleme hizmeti 'ni silecek.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="f4e3a-110">Depolama eşitleme hizmeti, yalnızca içerdiği tüm eşitleme grupları ve kaydedilmiş sunucular ilk kez silindiğinde kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="f4e3a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4e3a-111">EXAMPLES</span></span>

### <span data-ttu-id="f4e3a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4e3a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="f4e3a-113">Bu komut, depolama eşitleme hizmetini kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="f4e3a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4e3a-114">PARAMETERS</span></span>

### <span data-ttu-id="f4e3a-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="f4e3a-115">-AsJob</span></span>
<span data-ttu-id="f4e3a-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f4e3a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4e3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e3a-117">-DefaultProfile</span></span>
<span data-ttu-id="f4e3a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e3a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f4e3a-119">-Force</span></span>
<span data-ttu-id="f4e3a-120">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4e3a-121">-InputObject</span></span>
<span data-ttu-id="f4e3a-122">Normalde ardışık düzen aracılığıyla geçirilen StorageSyncService giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4e3a-123">-Name</span></span>
<span data-ttu-id="f4e3a-124">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f4e3a-125">-PassThru</span></span>
<span data-ttu-id="f4e3a-126">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f4e3a-127">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f4e3a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e3a-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4e3a-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f4e3a-130">-ResourceId</span></span>
<span data-ttu-id="f4e3a-131">StorageSyncService kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f4e3a-131">StorageSyncService Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e3a-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4e3a-132">-Confirm</span></span>
<span data-ttu-id="f4e3a-133">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e3a-134">-WhatIf</span></span>
<span data-ttu-id="f4e3a-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4e3a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e3a-137">CommonParameters</span></span>
<span data-ttu-id="f4e3a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4e3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e3a-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e3a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e3a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4e3a-140">INPUTS</span></span>

### <span data-ttu-id="f4e3a-141">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f4e3a-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="f4e3a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e3a-142">System.String</span></span>

### <span data-ttu-id="f4e3a-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4e3a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4e3a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4e3a-144">OUTPUTS</span></span>

### <span data-ttu-id="f4e3a-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="f4e3a-145">System.Object</span></span>
## <span data-ttu-id="f4e3a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4e3a-146">NOTES</span></span>

## <span data-ttu-id="f4e3a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4e3a-147">RELATED LINKS</span></span>
