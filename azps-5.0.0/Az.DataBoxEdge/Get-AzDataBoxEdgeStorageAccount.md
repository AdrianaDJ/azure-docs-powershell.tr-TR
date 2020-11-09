---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321226"
---
# <span data-ttu-id="231e8-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="231e8-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="231e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="231e8-102">SYNOPSIS</span></span>
<span data-ttu-id="231e8-103">Aygıttaki Edge depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="231e8-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="231e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="231e8-104">SYNTAX</span></span>

### <span data-ttu-id="231e8-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="231e8-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="231e8-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="231e8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="231e8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="231e8-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="231e8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="231e8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="231e8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="231e8-109">DESCRIPTION</span></span>
<span data-ttu-id="231e8-110">**Get-AzDataBoxEdgeStorageAccount** cmdlet 'i, bir veri kutusu uç cihazında kullanılabilen Edge depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="231e8-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="231e8-111">Belirli bir Edge depolama hesabının bilgilerini almak için adı cmdlet 'te parametre olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="231e8-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="231e8-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="231e8-112">EXAMPLES</span></span>

### <span data-ttu-id="231e8-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="231e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="231e8-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="231e8-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="231e8-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="231e8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="231e8-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="231e8-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="231e8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="231e8-117">PARAMETERS</span></span>

### <span data-ttu-id="231e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="231e8-118">-DefaultProfile</span></span>
<span data-ttu-id="231e8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="231e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="231e8-120">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="231e8-120">-DeviceName</span></span>
<span data-ttu-id="231e8-121">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="231e8-121">Device Name</span></span>

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

### <span data-ttu-id="231e8-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="231e8-122">-DeviceObject</span></span>
<span data-ttu-id="231e8-123">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="231e8-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="231e8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="231e8-124">-Name</span></span>
<span data-ttu-id="231e8-125">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="231e8-125">Resource Name</span></span>

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

### <span data-ttu-id="231e8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="231e8-126">-ResourceGroupName</span></span>
<span data-ttu-id="231e8-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="231e8-127">Resource Group Name</span></span>

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

### <span data-ttu-id="231e8-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="231e8-128">-ResourceId</span></span>
<span data-ttu-id="231e8-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="231e8-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="231e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="231e8-130">CommonParameters</span></span>
<span data-ttu-id="231e8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="231e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="231e8-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="231e8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="231e8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="231e8-133">INPUTS</span></span>

### <span data-ttu-id="231e8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="231e8-134">System.String</span></span>

### <span data-ttu-id="231e8-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="231e8-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="231e8-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="231e8-136">OUTPUTS</span></span>

### <span data-ttu-id="231e8-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="231e8-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="231e8-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="231e8-138">NOTES</span></span>

## <span data-ttu-id="231e8-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="231e8-139">RELATED LINKS</span></span>
