---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098608"
---
# <span data-ttu-id="59f71-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="59f71-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="59f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f71-102">SYNOPSIS</span></span>
<span data-ttu-id="59f71-103">Bu komut tüm katmanlı dosyaları yerel diske geri çeker.</span><span class="sxs-lookup"><span data-stu-id="59f71-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="59f71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59f71-104">SYNTAX</span></span>

### <span data-ttu-id="59f71-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59f71-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f71-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="59f71-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f71-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59f71-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f71-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59f71-108">DESCRIPTION</span></span>
<span data-ttu-id="59f71-109">Bir sunucu uç noktasında (kaydettirilmiş bir sunucuda belirli bir konumda) bulut özelliği etkinleştirildiğinde, bu komut tüm katmanlı dosyaları yerel diske geri çekmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="59f71-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="59f71-110">Geri çekmeyi başlatmadan önce bu sunucu uç noktasında bulut sunucusunu devre dışı bırakmanız kesinlikle önerilir.</span><span class="sxs-lookup"><span data-stu-id="59f71-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="59f71-111">Yine de açıksa, geri çekme özelliği, yerel diskte bulunan tüm içeriğin istenen hedefini elde etme</span><span class="sxs-lookup"><span data-stu-id="59f71-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="59f71-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59f71-112">EXAMPLES</span></span>

### <span data-ttu-id="59f71-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59f71-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="59f71-114">Bu komut, belirtilen sunucu uç noktasının kök yolunun altındaki tüm katmanlı dosyaları yinelemeli olarak geri çeker.</span><span class="sxs-lookup"><span data-stu-id="59f71-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="59f71-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59f71-115">PARAMETERS</span></span>

### <span data-ttu-id="59f71-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="59f71-116">-AsJob</span></span>
<span data-ttu-id="59f71-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="59f71-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59f71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f71-118">-DefaultProfile</span></span>
<span data-ttu-id="59f71-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59f71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f71-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59f71-120">-InputObject</span></span>
<span data-ttu-id="59f71-121">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="59f71-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59f71-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="59f71-122">-Name</span></span>
<span data-ttu-id="59f71-123">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="59f71-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f71-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59f71-124">-PassThru</span></span>
<span data-ttu-id="59f71-125">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="59f71-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="59f71-126">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="59f71-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="59f71-127">-Desen</span><span class="sxs-lookup"><span data-stu-id="59f71-127">-Pattern</span></span>
<span data-ttu-id="59f71-128">Dosya adının deseni</span><span class="sxs-lookup"><span data-stu-id="59f71-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="59f71-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="59f71-129">-RecallPath</span></span>
<span data-ttu-id="59f71-130">Geri çekme yolu</span><span class="sxs-lookup"><span data-stu-id="59f71-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="59f71-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f71-131">-ResourceGroupName</span></span>
<span data-ttu-id="59f71-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="59f71-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="59f71-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="59f71-133">-ResourceId</span></span>
<span data-ttu-id="59f71-134">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="59f71-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="59f71-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="59f71-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="59f71-136">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="59f71-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f71-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="59f71-137">-SyncGroupName</span></span>
<span data-ttu-id="59f71-138">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="59f71-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f71-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="59f71-139">-Confirm</span></span>
<span data-ttu-id="59f71-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59f71-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f71-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f71-141">-WhatIf</span></span>
<span data-ttu-id="59f71-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f71-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59f71-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59f71-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f71-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f71-144">CommonParameters</span></span>
<span data-ttu-id="59f71-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59f71-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f71-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f71-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f71-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59f71-147">INPUTS</span></span>

### <span data-ttu-id="59f71-148">System. String</span><span class="sxs-lookup"><span data-stu-id="59f71-148">System.String</span></span>

### <span data-ttu-id="59f71-149">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="59f71-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="59f71-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59f71-150">OUTPUTS</span></span>

### <span data-ttu-id="59f71-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59f71-151">System.Boolean</span></span>

## <span data-ttu-id="59f71-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59f71-152">NOTES</span></span>

## <span data-ttu-id="59f71-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59f71-153">RELATED LINKS</span></span>
