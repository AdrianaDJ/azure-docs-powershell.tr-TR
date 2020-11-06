---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 1bea5ce9eda22996eb65b6e5d26fb3af19cd1c88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589401"
---
# <span data-ttu-id="d8c23-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="d8c23-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="d8c23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c23-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c23-103">Çalışma alanı içinde bir depolama anlayış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8c23-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8c23-104">SYNTAX</span></span>

### <span data-ttu-id="d8c23-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8c23-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8c23-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="d8c23-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8c23-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8c23-107">DESCRIPTION</span></span>
<span data-ttu-id="d8c23-108">**Yeni-Azurermoperationalınsightsstorageınsight** cmdlet 'i, var olan bir çalışma alanında yeni bir depolama Insight oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8c23-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="d8c23-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8c23-109">EXAMPLES</span></span>

### <span data-ttu-id="d8c23-110">Örnek 1: adla bir depolama anlayış oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8c23-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="d8c23-111">İlk komut, ContosoStorage adlı depolama hesabını almak için Get-AzureRmStorageAccount cmdlet 'ini kullanır ve $Storage değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8c23-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="d8c23-112">İkinci komut $Storage Depolama hesabını, belirtilen depolama hesabı anahtarını almak için ardışık düzen işlecini kullanarak Get-AzureRmStorageAccountKey cmdlet 'ine geçirir ve ardından $StorageKey değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8c23-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="d8c23-113">Son komutu MyWorkspace adındaki Mystorageınsight adlı bir depolama Insight oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8c23-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="d8c23-114">Bu depolama bilgileri belirtilen depolama hesabı kaynağındaki WADWindowsEventLogsTable tablosundan verileri tüketir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="d8c23-115">Örnek 2: çalışma alanı nesnesi kullanarak depolama anlayış oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8c23-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="d8c23-116">İlk komut MyWorkspace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve $Workspace değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8c23-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="d8c23-117">İkinci komut, Get-AzureRmStorageAccount cmdlet 'ini kullanarak belirtilen depolama hesabını alır ve $Storage değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8c23-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="d8c23-118">Üçüncü komut Get-AzureRmStorageAccountKey $Storage Depolama hesabını, ardışık düzen işlecini kullanarak belirtilen anahtarı elde edin ve ardından $StorageKey değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8c23-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="d8c23-119">Son komutu, $Workspace tanımlı çalışma alanındaki Mystorageınsight adlı bir depolama Insight oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8c23-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="d8c23-120">Depolama anlayış, belirtilen depolama hesabı kaynağındaki WADWindowsEventLogsTable tablosundan verileri tüketir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="d8c23-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8c23-121">PARAMETERS</span></span>

### <span data-ttu-id="d8c23-122">-Kapsayıcılar</span><span class="sxs-lookup"><span data-stu-id="d8c23-122">-Containers</span></span>
<span data-ttu-id="d8c23-123">Verileri içeren kapsayıcıların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="d8c23-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c23-124">-DefaultProfile</span></span>
<span data-ttu-id="d8c23-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d8c23-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8c23-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d8c23-126">-Force</span></span>
<span data-ttu-id="d8c23-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d8c23-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8c23-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8c23-128">-Name</span></span>
<span data-ttu-id="d8c23-129">Depolama anlayış adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="d8c23-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c23-130">-ResourceGroupName</span></span>
<span data-ttu-id="d8c23-131">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d8c23-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8c23-132">-StorageAccountKey</span></span>
<span data-ttu-id="d8c23-133">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-133">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="d8c23-134">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="d8c23-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="d8c23-135">Depolama hesabının Azure kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="d8c23-136">Bu, Get-AzureRmStorageAccount cmdlet 'i yürüterek sonucun *ID* parametresine erişerek alınabilir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-136">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="d8c23-137">-Tablolar</span><span class="sxs-lookup"><span data-stu-id="d8c23-137">-Tables</span></span>
<span data-ttu-id="d8c23-138">Verileri sağlayan tabloların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="d8c23-139">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="d8c23-139">-Workspace</span></span>
<span data-ttu-id="d8c23-140">Yeni depolama anlayış çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="d8c23-141">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d8c23-141">-WorkspaceName</span></span>
<span data-ttu-id="d8c23-142">Var olan bir çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="d8c23-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8c23-143">-Confirm</span></span>
<span data-ttu-id="d8c23-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8c23-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c23-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c23-145">-WhatIf</span></span>
<span data-ttu-id="d8c23-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8c23-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c23-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8c23-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c23-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c23-148">CommonParameters</span></span>
<span data-ttu-id="d8c23-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8c23-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c23-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c23-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c23-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8c23-151">INPUTS</span></span>

### <span data-ttu-id="d8c23-152">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8c23-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d8c23-153">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d8c23-153">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="d8c23-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d8c23-154">System.String</span></span>

### <span data-ttu-id="d8c23-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="d8c23-155">System.String[]</span></span>

## <span data-ttu-id="d8c23-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8c23-156">OUTPUTS</span></span>

### <span data-ttu-id="d8c23-157">Microsoft. Azure. Commands. Operationalınsights. modeller. Psstorageınsight</span><span class="sxs-lookup"><span data-stu-id="d8c23-157">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="d8c23-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8c23-158">NOTES</span></span>

## <span data-ttu-id="d8c23-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8c23-159">RELATED LINKS</span></span>

[<span data-ttu-id="d8c23-160">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d8c23-160">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="d8c23-161">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="d8c23-161">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


