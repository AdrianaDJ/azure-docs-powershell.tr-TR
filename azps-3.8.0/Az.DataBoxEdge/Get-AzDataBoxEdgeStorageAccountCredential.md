---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098891"
---
# <span data-ttu-id="1c0d1-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1c0d1-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1c0d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0d1-103">Cihazdaki depolama hesabına karşılık gelen depolama hesabı kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1c0d1-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="1c0d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c0d1-104">SYNTAX</span></span>

### <span data-ttu-id="1c0d1-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c0d1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c0d1-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1c0d1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c0d1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c0d1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c0d1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c0d1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="1c0d1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c0d1-109">DESCRIPTION</span></span>
<span data-ttu-id="1c0d1-110">**Get-AzDataBoxEdgeStorageAccountCredential** cmdlet 'ı, veri kutusu Edge aygıtındaki ilgili depolama hesabının depolama hesabı kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1c0d1-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="1c0d1-111">Belirli bir depolama hesabı kimlik bilgisi hakkında bilgi almak için ad, kaynak grubu adı ve cihaz adı parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c0d1-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="1c0d1-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c0d1-112">EXAMPLES</span></span>

### <span data-ttu-id="1c0d1-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1c0d1-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="1c0d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c0d1-114">PARAMETERS</span></span>

### <span data-ttu-id="1c0d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0d1-115">-DefaultProfile</span></span>
<span data-ttu-id="1c0d1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c0d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c0d1-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="1c0d1-117">-DeviceName</span></span>
<span data-ttu-id="1c0d1-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="1c0d1-118">Device Name</span></span>

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

### <span data-ttu-id="1c0d1-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="1c0d1-119">-DeviceObject</span></span>
<span data-ttu-id="1c0d1-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="1c0d1-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="1c0d1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c0d1-121">-Name</span></span>
<span data-ttu-id="1c0d1-122">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="1c0d1-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="1c0d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c0d1-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1c0d1-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1c0d1-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1c0d1-125">-ResourceId</span></span>
<span data-ttu-id="1c0d1-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1c0d1-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1c0d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0d1-127">CommonParameters</span></span>
<span data-ttu-id="1c0d1-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c0d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0d1-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1c0d1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0d1-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c0d1-130">INPUTS</span></span>

### <span data-ttu-id="1c0d1-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1c0d1-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1c0d1-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c0d1-132">OUTPUTS</span></span>

### <span data-ttu-id="1c0d1-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1c0d1-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1c0d1-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c0d1-134">NOTES</span></span>

## <span data-ttu-id="1c0d1-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c0d1-135">RELATED LINKS</span></span>
