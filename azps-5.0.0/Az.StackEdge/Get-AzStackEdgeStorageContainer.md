---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279583"
---
# <span data-ttu-id="db5c0-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db5c0-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="db5c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="db5c0-103">Cihazda bir Edge depolama hesabı için kapsayıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="db5c0-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="db5c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db5c0-104">SYNTAX</span></span>

### <span data-ttu-id="db5c0-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db5c0-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db5c0-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="db5c0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db5c0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5c0-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db5c0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5c0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="db5c0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="db5c0-109">DESCRIPTION</span></span>
<span data-ttu-id="db5c0-110">**Get-AzStackEdgeStorageContainer** cmdlet 'ı, yığın uç cihazında bir Edge depolama hesabı için depolama kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="db5c0-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="db5c0-111">Belirli bir depolama kapsayıcısının ayrıntılarını getirmek için adı cmdlet 'te parametre olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db5c0-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="db5c0-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db5c0-112">EXAMPLES</span></span>

### <span data-ttu-id="db5c0-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="db5c0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="db5c0-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="db5c0-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="db5c0-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="db5c0-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="db5c0-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db5c0-116">PARAMETERS</span></span>

### <span data-ttu-id="db5c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5c0-117">-DefaultProfile</span></span>
<span data-ttu-id="db5c0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db5c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db5c0-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="db5c0-119">-DeviceName</span></span>
<span data-ttu-id="db5c0-120">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="db5c0-120">Device Name</span></span>

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

### <span data-ttu-id="db5c0-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db5c0-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="db5c0-122">Var olan EdgeStorageAccount adının adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="db5c0-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="db5c0-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="db5c0-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="db5c0-124">Var olan EdgeStorageAccount nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="db5c0-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="db5c0-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="db5c0-125">-Name</span></span>
<span data-ttu-id="db5c0-126">EdgeStorageContainer adı</span><span class="sxs-lookup"><span data-stu-id="db5c0-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="db5c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="db5c0-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="db5c0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="db5c0-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="db5c0-129">-ResourceId</span></span>
<span data-ttu-id="db5c0-130">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="db5c0-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="db5c0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5c0-131">CommonParameters</span></span>
<span data-ttu-id="db5c0-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db5c0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5c0-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db5c0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5c0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db5c0-134">INPUTS</span></span>

### <span data-ttu-id="db5c0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="db5c0-135">System.String</span></span>

### <span data-ttu-id="db5c0-136">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db5c0-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="db5c0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db5c0-137">OUTPUTS</span></span>

### <span data-ttu-id="db5c0-138">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db5c0-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="db5c0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db5c0-139">NOTES</span></span>

## <span data-ttu-id="db5c0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db5c0-140">RELATED LINKS</span></span>
