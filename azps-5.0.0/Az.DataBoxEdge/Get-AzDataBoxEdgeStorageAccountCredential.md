---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321225"
---
# <span data-ttu-id="a39fa-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a39fa-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a39fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a39fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a39fa-103">Cihazdaki depolama hesabına karşılık gelen depolama hesabı kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a39fa-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="a39fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a39fa-104">SYNTAX</span></span>

### <span data-ttu-id="a39fa-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a39fa-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a39fa-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a39fa-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a39fa-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a39fa-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a39fa-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a39fa-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a39fa-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a39fa-109">DESCRIPTION</span></span>
<span data-ttu-id="a39fa-110">**Get-AzDataBoxEdgeStorageAccountCredential** cmdlet 'ı, veri kutusu Edge aygıtındaki ilgili depolama hesabının depolama hesabı kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a39fa-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="a39fa-111">Belirli bir depolama hesabı kimlik bilgisi hakkında bilgi almak için ad, kaynak grubu adı ve cihaz adı parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a39fa-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="a39fa-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a39fa-112">EXAMPLES</span></span>

### <span data-ttu-id="a39fa-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a39fa-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="a39fa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a39fa-114">PARAMETERS</span></span>

### <span data-ttu-id="a39fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39fa-115">-DefaultProfile</span></span>
<span data-ttu-id="a39fa-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a39fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39fa-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="a39fa-117">-DeviceName</span></span>
<span data-ttu-id="a39fa-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="a39fa-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39fa-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a39fa-119">-DeviceObject</span></span>
<span data-ttu-id="a39fa-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="a39fa-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a39fa-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a39fa-121">-Name</span></span>
<span data-ttu-id="a39fa-122">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="a39fa-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="a39fa-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a39fa-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39fa-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a39fa-125">-ResourceId</span></span>
<span data-ttu-id="a39fa-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a39fa-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39fa-127">CommonParameters</span></span>
<span data-ttu-id="a39fa-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a39fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39fa-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a39fa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39fa-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a39fa-130">INPUTS</span></span>

### <span data-ttu-id="a39fa-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a39fa-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a39fa-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a39fa-132">OUTPUTS</span></span>

### <span data-ttu-id="a39fa-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a39fa-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a39fa-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a39fa-134">NOTES</span></span>

## <span data-ttu-id="a39fa-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a39fa-135">RELATED LINKS</span></span>
