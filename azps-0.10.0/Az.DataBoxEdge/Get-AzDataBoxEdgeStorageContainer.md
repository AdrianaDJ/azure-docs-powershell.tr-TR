---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 174f6c58dfeb2d79a19b08cc1f360ea05e0c4736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936783"
---
# <span data-ttu-id="d61f4-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d61f4-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d61f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d61f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d61f4-103">Cihazda bir Edge depolama hesabı için kapsayıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="d61f4-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="d61f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d61f4-104">SYNTAX</span></span>

### <span data-ttu-id="d61f4-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d61f4-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d61f4-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d61f4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d61f4-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d61f4-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d61f4-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d61f4-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="d61f4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d61f4-109">DESCRIPTION</span></span>
<span data-ttu-id="d61f4-110">**Get-AzDataBoxEdgeStorageContainer** cmdlet 'i, bir veri kutusu uç aygıtındaki bir Edge depolama hesabı için depolama kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="d61f4-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="d61f4-111">Belirli bir depolama kapsayıcısının ayrıntılarını getirmek için adı cmdlet 'te parametre olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d61f4-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="d61f4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d61f4-112">EXAMPLES</span></span>

### <span data-ttu-id="d61f4-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d61f4-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d61f4-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d61f4-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d61f4-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d61f4-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="d61f4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d61f4-116">PARAMETERS</span></span>

### <span data-ttu-id="d61f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61f4-117">-DefaultProfile</span></span>
<span data-ttu-id="d61f4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d61f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d61f4-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="d61f4-119">-DeviceName</span></span>
<span data-ttu-id="d61f4-120">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="d61f4-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d61f4-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d61f4-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="d61f4-122">Var olan EdgeStorageAccount adının adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="d61f4-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d61f4-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="d61f4-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="d61f4-124">Var olan EdgeStorageAccount nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="d61f4-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d61f4-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="d61f4-125">-Name</span></span>
<span data-ttu-id="d61f4-126">EdgeStorageContainer adı</span><span class="sxs-lookup"><span data-stu-id="d61f4-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d61f4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61f4-127">-ResourceGroupName</span></span>
<span data-ttu-id="d61f4-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d61f4-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d61f4-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d61f4-129">-ResourceId</span></span>
<span data-ttu-id="d61f4-130">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d61f4-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d61f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61f4-131">CommonParameters</span></span>
<span data-ttu-id="d61f4-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d61f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61f4-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d61f4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61f4-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d61f4-134">INPUTS</span></span>

### <span data-ttu-id="d61f4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d61f4-135">System.String</span></span>

### <span data-ttu-id="d61f4-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d61f4-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="d61f4-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d61f4-137">OUTPUTS</span></span>

### <span data-ttu-id="d61f4-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d61f4-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d61f4-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d61f4-139">NOTES</span></span>

## <span data-ttu-id="d61f4-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d61f4-140">RELATED LINKS</span></span>