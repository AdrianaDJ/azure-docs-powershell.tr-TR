---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109730"
---
# <span data-ttu-id="40d72-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="40d72-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="40d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d72-102">SYNOPSIS</span></span>
<span data-ttu-id="40d72-103">Databox Işleri hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="40d72-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="40d72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40d72-104">SYNTAX</span></span>

### <span data-ttu-id="40d72-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40d72-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40d72-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d72-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40d72-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="40d72-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="40d72-108">DESCRIPTION</span></span>
<span data-ttu-id="40d72-109">**Get-AzDataBoxJobs** cmdlet 'ı bir Azure aboneliğindeki databox işleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="40d72-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="40d72-110">Kaynak grubu belirtirseniz, bu cmdlet bu kaynak grubu altındaki tüm veri kutusu işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="40d72-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="40d72-111">İşin adını kaynak grubu adıyla birlikte belirtirseniz, bu cmdlet o belirli veri kutusu işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="40d72-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="40d72-112">Abonelik kimliği dışında hiçbir şey belirtmezseniz, bu cmdlet bu aboneliğin altındaki tüm veri kutusu işleriyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="40d72-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="40d72-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40d72-113">EXAMPLES</span></span>

### <span data-ttu-id="40d72-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="40d72-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="40d72-115">Herhangi bir parametre olmadan Get-AzDataBoxJob aboneliğin altındaki tüm veri kutusu işlerini getirir</span><span class="sxs-lookup"><span data-stu-id="40d72-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="40d72-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="40d72-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="40d72-117">ResourceGroupName parametresiyle birlikte Get-AzDataBoxJob belirtilen kaynak grubu altındaki tüm veri kutusu işlerini getirir</span><span class="sxs-lookup"><span data-stu-id="40d72-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="40d72-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="40d72-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="40d72-119">Belirtilen ResourceGroupName ve adı ile Get-AzDataBoxJob bu belirli veri kutusu işini getirir</span><span class="sxs-lookup"><span data-stu-id="40d72-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="40d72-120">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="40d72-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="40d72-121">RESOURCEID ile belirtilen Get-AzDataBoxJob, bu belirli veri kutusu işini getirir</span><span class="sxs-lookup"><span data-stu-id="40d72-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="40d72-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40d72-122">PARAMETERS</span></span>

### <span data-ttu-id="40d72-123">-İptal edildi</span><span class="sxs-lookup"><span data-stu-id="40d72-123">-Aborted</span></span>
<span data-ttu-id="40d72-124">Durdurulan işlere parametre geçme</span><span class="sxs-lookup"><span data-stu-id="40d72-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d72-125">-İptal edildi</span><span class="sxs-lookup"><span data-stu-id="40d72-125">-Cancelled</span></span>
<span data-ttu-id="40d72-126">Iptal edilen işleri getirmek için parametre değiştirme</span><span class="sxs-lookup"><span data-stu-id="40d72-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d72-127">-Tamamlandı</span><span class="sxs-lookup"><span data-stu-id="40d72-127">-Completed</span></span>
<span data-ttu-id="40d72-128">Tamamlanan işleri getirmek için parametreyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="40d72-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d72-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="40d72-129">-CompletedWithError</span></span>
<span data-ttu-id="40d72-130">Hatalarla tamamlanan getirme işlerine geçme</span><span class="sxs-lookup"><span data-stu-id="40d72-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d72-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d72-131">-DefaultProfile</span></span>
<span data-ttu-id="40d72-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40d72-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d72-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="40d72-133">-Name</span></span>
<span data-ttu-id="40d72-134">Databox Iş adı</span><span class="sxs-lookup"><span data-stu-id="40d72-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d72-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d72-135">-ResourceGroupName</span></span>
<span data-ttu-id="40d72-136">Databox Iş kaynağı grubu adı</span><span class="sxs-lookup"><span data-stu-id="40d72-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d72-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="40d72-137">-ResourceId</span></span>
<span data-ttu-id="40d72-138">Databox Iş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="40d72-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d72-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d72-139">CommonParameters</span></span>
<span data-ttu-id="40d72-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40d72-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d72-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40d72-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d72-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40d72-142">INPUTS</span></span>

### <span data-ttu-id="40d72-143">System. String</span><span class="sxs-lookup"><span data-stu-id="40d72-143">System.String</span></span>

## <span data-ttu-id="40d72-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40d72-144">OUTPUTS</span></span>

### <span data-ttu-id="40d72-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="40d72-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="40d72-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40d72-146">NOTES</span></span>

## <span data-ttu-id="40d72-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40d72-147">RELATED LINKS</span></span>
