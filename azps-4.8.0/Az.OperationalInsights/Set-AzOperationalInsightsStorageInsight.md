---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268419"
---
# <span data-ttu-id="a5ce9-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a5ce9-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="a5ce9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ce9-103">Bir depolama Insight güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="a5ce9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5ce9-104">SYNTAX</span></span>

### <span data-ttu-id="a5ce9-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5ce9-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5ce9-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="a5ce9-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5ce9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5ce9-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ce9-108">**Set-Azişlemkimliği** , bir depolama Insight yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="a5ce9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5ce9-109">EXAMPLES</span></span>

### <span data-ttu-id="a5ce9-110">Örnek 1: adla bir depolama kavramı değiştirme</span><span class="sxs-lookup"><span data-stu-id="a5ce9-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="a5ce9-111">Bu komut Mystorageınsight adındaki depolama kavramasındaki tabloları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="a5ce9-112">Örnek 2: çalışma alanı nesnesi kullanarak bir depolama anlayış değiştirme</span><span class="sxs-lookup"><span data-stu-id="a5ce9-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="a5ce9-113">İlk komut MyWorkspace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve $Workspace değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="a5ce9-114">İkinci komut Mystorageınsight adındaki depolama kavramasındaki kapsayıcıları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="a5ce9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5ce9-115">PARAMETERS</span></span>

### <span data-ttu-id="a5ce9-116">-Kapsayıcılar</span><span class="sxs-lookup"><span data-stu-id="a5ce9-116">-Containers</span></span>
<span data-ttu-id="a5ce9-117">Verileri sağlayan kapsayıcıların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="a5ce9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ce9-118">-DefaultProfile</span></span>
<span data-ttu-id="a5ce9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a5ce9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5ce9-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5ce9-120">-Name</span></span>
<span data-ttu-id="a5ce9-121">Bir depolama anlayış adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="a5ce9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ce9-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5ce9-123">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="a5ce9-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a5ce9-124">-StorageAccountKey</span></span>
<span data-ttu-id="a5ce9-125">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ce9-126">-Tablolar</span><span class="sxs-lookup"><span data-stu-id="a5ce9-126">-Tables</span></span>
<span data-ttu-id="a5ce9-127">Verileri içeren tabloların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ce9-128">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="a5ce9-128">-Workspace</span></span>
<span data-ttu-id="a5ce9-129">Depolama kavramı içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="a5ce9-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="a5ce9-130">-WorkspaceName</span></span>
<span data-ttu-id="a5ce9-131">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="a5ce9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ce9-132">CommonParameters</span></span>
<span data-ttu-id="a5ce9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5ce9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ce9-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ce9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ce9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5ce9-135">INPUTS</span></span>

### <span data-ttu-id="a5ce9-136">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5ce9-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a5ce9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a5ce9-137">System.String</span></span>

### <span data-ttu-id="a5ce9-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="a5ce9-138">System.String[]</span></span>

## <span data-ttu-id="a5ce9-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5ce9-139">OUTPUTS</span></span>

### <span data-ttu-id="a5ce9-140">Microsoft. Azure. Commands. Operationalınsights. modeller. Psstorageınsight</span><span class="sxs-lookup"><span data-stu-id="a5ce9-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="a5ce9-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5ce9-141">NOTES</span></span>

## <span data-ttu-id="a5ce9-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5ce9-142">RELATED LINKS</span></span>

[<span data-ttu-id="a5ce9-143">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a5ce9-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="a5ce9-144">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="a5ce9-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


