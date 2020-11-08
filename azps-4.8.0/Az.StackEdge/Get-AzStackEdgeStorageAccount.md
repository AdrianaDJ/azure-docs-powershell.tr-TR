---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266274"
---
# <span data-ttu-id="a0d85-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0d85-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="a0d85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0d85-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d85-103">Aygıttaki Edge depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="a0d85-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="a0d85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0d85-104">SYNTAX</span></span>

### <span data-ttu-id="a0d85-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0d85-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0d85-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a0d85-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0d85-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d85-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0d85-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d85-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a0d85-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0d85-109">DESCRIPTION</span></span>
<span data-ttu-id="a0d85-110">**Get-AzStackEdgeStorageAccount** cmdlet 'ı, yığın uç cihazında kullanılabilen Edge depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="a0d85-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="a0d85-111">Belirli bir Edge depolama hesabının bilgilerini almak için adı cmdlet 'te parametre olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0d85-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="a0d85-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0d85-112">EXAMPLES</span></span>

### <span data-ttu-id="a0d85-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a0d85-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="a0d85-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a0d85-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="a0d85-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a0d85-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="a0d85-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a0d85-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="a0d85-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0d85-117">PARAMETERS</span></span>

### <span data-ttu-id="a0d85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d85-118">-DefaultProfile</span></span>
<span data-ttu-id="a0d85-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0d85-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0d85-120">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="a0d85-120">-DeviceName</span></span>
<span data-ttu-id="a0d85-121">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="a0d85-121">Device Name</span></span>

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

### <span data-ttu-id="a0d85-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a0d85-122">-DeviceObject</span></span>
<span data-ttu-id="a0d85-123">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="a0d85-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d85-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0d85-124">-Name</span></span>
<span data-ttu-id="a0d85-125">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="a0d85-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d85-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0d85-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a0d85-127">Resource Group Name</span></span>

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

### <span data-ttu-id="a0d85-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a0d85-128">-ResourceId</span></span>
<span data-ttu-id="a0d85-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a0d85-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="a0d85-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d85-130">CommonParameters</span></span>
<span data-ttu-id="a0d85-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0d85-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d85-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0d85-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d85-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0d85-133">INPUTS</span></span>

### <span data-ttu-id="a0d85-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a0d85-134">System.String</span></span>

### <span data-ttu-id="a0d85-135">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a0d85-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a0d85-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0d85-136">OUTPUTS</span></span>

### <span data-ttu-id="a0d85-137">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0d85-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="a0d85-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0d85-138">NOTES</span></span>

## <span data-ttu-id="a0d85-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0d85-139">RELATED LINKS</span></span>
