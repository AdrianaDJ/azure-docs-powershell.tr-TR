---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096534"
---
# <span data-ttu-id="78ddd-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="78ddd-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="78ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="78ddd-103">Cihazdaki depolama hesabına karşılık gelen depolama hesabı kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="78ddd-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="78ddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78ddd-104">SYNTAX</span></span>

### <span data-ttu-id="78ddd-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78ddd-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78ddd-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="78ddd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78ddd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78ddd-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78ddd-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78ddd-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="78ddd-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="78ddd-109">DESCRIPTION</span></span>
<span data-ttu-id="78ddd-110">**Get-AzStackEdgeStorageAccountCredential** cmdlet 'ı, yığın uç cihazında ilgili depolama hesabının depolama hesabı kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="78ddd-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="78ddd-111">Belirli bir depolama hesabı kimlik bilgisi hakkında bilgi almak için ad, kaynak grubu adı ve cihaz adı parametrelerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="78ddd-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="78ddd-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78ddd-112">EXAMPLES</span></span>

### <span data-ttu-id="78ddd-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="78ddd-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="78ddd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78ddd-114">PARAMETERS</span></span>

### <span data-ttu-id="78ddd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ddd-115">-DefaultProfile</span></span>
<span data-ttu-id="78ddd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78ddd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78ddd-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="78ddd-117">-DeviceName</span></span>
<span data-ttu-id="78ddd-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="78ddd-118">Device Name</span></span>

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

### <span data-ttu-id="78ddd-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="78ddd-119">-DeviceObject</span></span>
<span data-ttu-id="78ddd-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="78ddd-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="78ddd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="78ddd-121">-Name</span></span>
<span data-ttu-id="78ddd-122">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="78ddd-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78ddd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ddd-123">-ResourceGroupName</span></span>
<span data-ttu-id="78ddd-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="78ddd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="78ddd-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="78ddd-125">-ResourceId</span></span>
<span data-ttu-id="78ddd-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="78ddd-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="78ddd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ddd-127">CommonParameters</span></span>
<span data-ttu-id="78ddd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78ddd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ddd-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="78ddd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ddd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78ddd-130">INPUTS</span></span>

### <span data-ttu-id="78ddd-131">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="78ddd-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="78ddd-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78ddd-132">OUTPUTS</span></span>

### <span data-ttu-id="78ddd-133">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="78ddd-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="78ddd-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78ddd-134">NOTES</span></span>

## <span data-ttu-id="78ddd-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78ddd-135">RELATED LINKS</span></span>
