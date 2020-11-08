---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109415"
---
# <span data-ttu-id="b5ec4-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b5ec4-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="b5ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ec4-103">Çalışma alanı içinde bir depolama anlayış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="b5ec4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5ec4-104">SYNTAX</span></span>

### <span data-ttu-id="b5ec4-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5ec4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5ec4-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="b5ec4-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ec4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5ec4-107">DESCRIPTION</span></span>
<span data-ttu-id="b5ec4-108">**Yeni-Azişlemkimliği** , var olan bir çalışma alanında yeni bir depolama Insight oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="b5ec4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5ec4-109">EXAMPLES</span></span>

### <span data-ttu-id="b5ec4-110">Örnek 1: adla bir depolama anlayış oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5ec4-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="b5ec4-111">İlk komut, ContosoStorage adlı depolama hesabını almak için Get-AzStorageAccount cmdlet 'ini kullanır ve $Storage değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="b5ec4-112">İkinci komut $Storage Depolama hesabını, belirtilen depolama hesabı anahtarını almak için ardışık düzen işlecini kullanarak Get-AzStorageAccountKey cmdlet 'ine geçirir ve ardından $StorageKey değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="b5ec4-113">Bu örnek ilk anahtarı alır.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-113">This example retrieves the first key.</span></span> <span data-ttu-id="b5ec4-114">Diğerini geri almak için [0] değeri yerine [1] değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="b5ec4-115">Son komutu MyWorkspace adındaki Mystorageınsight adlı bir depolama Insight oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="b5ec4-116">Bu depolama bilgileri belirtilen depolama hesabı kaynağındaki WADWindowsEventLogsTable tablosundan verileri tüketir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="b5ec4-117">Örnek 2: çalışma alanı nesnesi kullanarak depolama anlayış oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5ec4-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="b5ec4-118">İlk komut MyWorkspace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve $Workspace değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="b5ec4-119">İkinci komut, Get-AzStorageAccount cmdlet 'ini kullanarak belirtilen depolama hesabını alır ve $Storage değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="b5ec4-120">Üçüncü komut Get-AzStorageAccountKey $Storage Depolama hesabını, ardışık düzen işlecini kullanarak belirtilen anahtarı elde edin ve ardından $StorageKey değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="b5ec4-121">Bu örnek ilk anahtarı alır.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-121">This example retrieves the first key.</span></span> <span data-ttu-id="b5ec4-122">Diğerini geri almak için [0] değeri yerine [1] değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="b5ec4-123">Son komutu, $Workspace tanımlı çalışma alanındaki Mystorageınsight adlı bir depolama Insight oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="b5ec4-124">Depolama anlayış, belirtilen depolama hesabı kaynağındaki WADWindowsEventLogsTable tablosundan verileri tüketir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="b5ec4-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5ec4-125">PARAMETERS</span></span>

### <span data-ttu-id="b5ec4-126">-Kapsayıcılar</span><span class="sxs-lookup"><span data-stu-id="b5ec4-126">-Containers</span></span>
<span data-ttu-id="b5ec4-127">Verileri içeren kapsayıcıların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-127">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ec4-128">-DefaultProfile</span></span>
<span data-ttu-id="b5ec4-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b5ec4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5ec4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b5ec4-130">-Force</span></span>
<span data-ttu-id="b5ec4-131">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5ec4-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5ec4-132">-Name</span></span>
<span data-ttu-id="b5ec4-133">Depolama anlayış adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-133">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ec4-134">-ResourceGroupName</span></span>
<span data-ttu-id="b5ec4-135">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b5ec4-136">-StorageAccountKey</span></span>
<span data-ttu-id="b5ec4-137">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-138">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="b5ec4-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="b5ec4-139">Depolama hesabının Azure kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="b5ec4-140">Bu, Get-AzStorageAccount cmdlet 'i yürüterek sonucun *ID* parametresine erişerek alınabilir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-141">-Tablolar</span><span class="sxs-lookup"><span data-stu-id="b5ec4-141">-Tables</span></span>
<span data-ttu-id="b5ec4-142">Verileri sağlayan tabloların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-142">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-143">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="b5ec4-143">-Workspace</span></span>
<span data-ttu-id="b5ec4-144">Yeni depolama anlayış çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-144">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-145">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b5ec4-145">-WorkspaceName</span></span>
<span data-ttu-id="b5ec4-146">Var olan bir çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-146">Specifies the name of an existing workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ec4-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5ec4-147">-Confirm</span></span>
<span data-ttu-id="b5ec4-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ec4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ec4-149">-WhatIf</span></span>
<span data-ttu-id="b5ec4-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ec4-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ec4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ec4-152">CommonParameters</span></span>
<span data-ttu-id="b5ec4-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5ec4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ec4-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ec4-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ec4-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5ec4-155">INPUTS</span></span>

### <span data-ttu-id="b5ec4-156">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5ec4-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b5ec4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b5ec4-157">System.String</span></span>

### <span data-ttu-id="b5ec4-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="b5ec4-158">System.String[]</span></span>

## <span data-ttu-id="b5ec4-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5ec4-159">OUTPUTS</span></span>

### <span data-ttu-id="b5ec4-160">Microsoft. Azure. Commands. Operationalınsights. modeller. Psstorageınsight</span><span class="sxs-lookup"><span data-stu-id="b5ec4-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="b5ec4-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5ec4-161">NOTES</span></span>

## <span data-ttu-id="b5ec4-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5ec4-162">RELATED LINKS</span></span>

[<span data-ttu-id="b5ec4-163">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b5ec4-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="b5ec4-164">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="b5ec4-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


