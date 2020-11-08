---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 65a48a000e5b3e4377ca2518992ad80242f9e4d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096716"
---
# <span data-ttu-id="cbdba-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cbdba-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="cbdba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbdba-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdba-103">Azure depolama blob Hizmetleri için hizmet özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cbdba-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="cbdba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbdba-104">SYNTAX</span></span>

### <span data-ttu-id="cbdba-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cbdba-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbdba-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cbdba-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbdba-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="cbdba-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbdba-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbdba-108">DESCRIPTION</span></span>
<span data-ttu-id="cbdba-109">**Get-AzStorageBlobServiceProperty** cmdlet 'ı, Azure depolama blob Hizmetleri için hizmet özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cbdba-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="cbdba-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbdba-110">EXAMPLES</span></span>

### <span data-ttu-id="cbdba-111">Örnek 1: belirtilen depolama hesabının Azure depolama blob Hizmetleri özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="cbdba-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days 
------------------ ----------------- --------------------- ----------------------------- -------------------------- 
myresourcegroup    mystorageaccount  2018-03-28            False                                                    
```

<span data-ttu-id="cbdba-112">Bu komut, belirtilen depolama hesabının blob Hizmetleri özelliğini alır.</span><span class="sxs-lookup"><span data-stu-id="cbdba-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="cbdba-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbdba-113">PARAMETERS</span></span>

### <span data-ttu-id="cbdba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdba-114">-DefaultProfile</span></span>
<span data-ttu-id="cbdba-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbdba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdba-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdba-116">-ResourceGroupName</span></span>
<span data-ttu-id="cbdba-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cbdba-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdba-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cbdba-118">-ResourceId</span></span>
<span data-ttu-id="cbdba-119">Blob hizmeti özellikleri kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cbdba-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdba-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cbdba-120">-StorageAccount</span></span>
<span data-ttu-id="cbdba-121">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="cbdba-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdba-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cbdba-122">-StorageAccountName</span></span>
<span data-ttu-id="cbdba-123">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="cbdba-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdba-124">CommonParameters</span></span>
<span data-ttu-id="cbdba-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbdba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdba-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbdba-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdba-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbdba-127">INPUTS</span></span>

### <span data-ttu-id="cbdba-128">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cbdba-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cbdba-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cbdba-129">System.String</span></span>

## <span data-ttu-id="cbdba-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbdba-130">OUTPUTS</span></span>

### <span data-ttu-id="cbdba-131">Microsoft. Azure. Commands. Management. Storage. model. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="cbdba-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="cbdba-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbdba-132">NOTES</span></span>

## <span data-ttu-id="cbdba-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbdba-133">RELATED LINKS</span></span>