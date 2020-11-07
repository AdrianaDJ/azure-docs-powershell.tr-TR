---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758493"
---
# <span data-ttu-id="b7fb2-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="b7fb2-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="b7fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fb2-103">Bu komut tüm katmanlı dosyaları yerel diske geri çeker.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="b7fb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7fb2-104">SYNTAX</span></span>

### <span data-ttu-id="b7fb2-105">ObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7fb2-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7fb2-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7fb2-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7fb2-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b7fb2-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7fb2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7fb2-108">DESCRIPTION</span></span>
<span data-ttu-id="b7fb2-109">Bir sunucu uç noktasında (kaydettirilmiş bir sunucuda belirli bir konumda) bulut özelliği etkinleştirildiğinde, bu komut tüm katmanlı dosyaları yerel diske geri çekmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="b7fb2-110">Geri çekmeyi başlatmadan önce bu sunucu uç noktasında bulut sunucusunu devre dışı bırakmanız kesinlikle önerilir.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="b7fb2-111">Yine de açıksa, geri çekme özelliği, yerel diskte bulunan tüm içeriğin istenen hedefini elde etme</span><span class="sxs-lookup"><span data-stu-id="b7fb2-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="b7fb2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7fb2-112">EXAMPLES</span></span>

### <span data-ttu-id="b7fb2-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7fb2-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="b7fb2-114">Bu komut, belirtilen sunucu uç noktasının kök yolunun altındaki tüm katmanlı dosyaları yinelemeli olarak geri çeker.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="b7fb2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7fb2-115">PARAMETERS</span></span>

### <span data-ttu-id="b7fb2-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="b7fb2-116">-AsJob</span></span>
<span data-ttu-id="b7fb2-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b7fb2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7fb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fb2-118">-DefaultProfile</span></span>
<span data-ttu-id="b7fb2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fb2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7fb2-120">-InputObject</span></span>
<span data-ttu-id="b7fb2-121">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fb2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7fb2-122">-Name</span></span>
<span data-ttu-id="b7fb2-123">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="b7fb2-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b7fb2-124">-PassThru</span></span>
<span data-ttu-id="b7fb2-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="b7fb2-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b7fb2-126">-Desen</span><span class="sxs-lookup"><span data-stu-id="b7fb2-126">-Pattern</span></span>
<span data-ttu-id="b7fb2-127">Dosya adının deseni</span><span class="sxs-lookup"><span data-stu-id="b7fb2-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="b7fb2-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="b7fb2-128">-RecallPath</span></span>
<span data-ttu-id="b7fb2-129">Geri çekme yolu</span><span class="sxs-lookup"><span data-stu-id="b7fb2-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="b7fb2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fb2-130">-ResourceGroupName</span></span>
<span data-ttu-id="b7fb2-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7fb2-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b7fb2-132">-ResourceId</span></span>
<span data-ttu-id="b7fb2-133">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b7fb2-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="b7fb2-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b7fb2-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="b7fb2-135">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b7fb2-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fb2-136">-SyncGroupName</span></span>
<span data-ttu-id="b7fb2-137">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="b7fb2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fb2-138">CommonParameters</span></span>
<span data-ttu-id="b7fb2-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7fb2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fb2-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7fb2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fb2-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7fb2-141">INPUTS</span></span>

### <span data-ttu-id="b7fb2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b7fb2-142">System.String</span></span>

### <span data-ttu-id="b7fb2-143">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7fb2-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="b7fb2-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7fb2-144">OUTPUTS</span></span>

### <span data-ttu-id="b7fb2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7fb2-145">System.Boolean</span></span>

## <span data-ttu-id="b7fb2-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7fb2-146">NOTES</span></span>

## <span data-ttu-id="b7fb2-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7fb2-147">RELATED LINKS</span></span>
