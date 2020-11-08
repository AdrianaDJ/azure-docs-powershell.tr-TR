---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096529"
---
# <span data-ttu-id="6184c-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6184c-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6184c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6184c-102">SYNOPSIS</span></span>
<span data-ttu-id="6184c-103">Cihazda bir Edge depolama hesabı için kapsayıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="6184c-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="6184c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6184c-104">SYNTAX</span></span>

### <span data-ttu-id="6184c-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6184c-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6184c-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6184c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6184c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6184c-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6184c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6184c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="6184c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6184c-109">DESCRIPTION</span></span>
<span data-ttu-id="6184c-110">**Get-AzStackEdgeStorageContainer** cmdlet 'ı, yığın uç cihazında bir Edge depolama hesabı için depolama kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="6184c-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="6184c-111">Belirli bir depolama kapsayıcısının ayrıntılarını getirmek için adı cmdlet 'te parametre olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6184c-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="6184c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6184c-112">EXAMPLES</span></span>

### <span data-ttu-id="6184c-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6184c-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="6184c-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6184c-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="6184c-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6184c-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="6184c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6184c-116">PARAMETERS</span></span>

### <span data-ttu-id="6184c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6184c-117">-DefaultProfile</span></span>
<span data-ttu-id="6184c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6184c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6184c-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="6184c-119">-DeviceName</span></span>
<span data-ttu-id="6184c-120">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="6184c-120">Device Name</span></span>

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

### <span data-ttu-id="6184c-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6184c-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="6184c-122">Var olan EdgeStorageAccount adının adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="6184c-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="6184c-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="6184c-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="6184c-124">Var olan EdgeStorageAccount nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="6184c-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6184c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="6184c-125">-Name</span></span>
<span data-ttu-id="6184c-126">EdgeStorageContainer adı</span><span class="sxs-lookup"><span data-stu-id="6184c-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="6184c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6184c-127">-ResourceGroupName</span></span>
<span data-ttu-id="6184c-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6184c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="6184c-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6184c-129">-ResourceId</span></span>
<span data-ttu-id="6184c-130">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6184c-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="6184c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6184c-131">CommonParameters</span></span>
<span data-ttu-id="6184c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6184c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6184c-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6184c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6184c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6184c-134">INPUTS</span></span>

### <span data-ttu-id="6184c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6184c-135">System.String</span></span>

### <span data-ttu-id="6184c-136">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6184c-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="6184c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6184c-137">OUTPUTS</span></span>

### <span data-ttu-id="6184c-138">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6184c-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6184c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6184c-139">NOTES</span></span>

## <span data-ttu-id="6184c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6184c-140">RELATED LINKS</span></span>
