---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 03e77346c14e095a11720b8cdaf930eaaa397f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758671"
---
# <span data-ttu-id="3ae61-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3ae61-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="3ae61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae61-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae61-103">Azure depolama blob Hizmetleri için hizmet özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ae61-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="3ae61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ae61-104">SYNTAX</span></span>

### <span data-ttu-id="3ae61-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ae61-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ae61-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3ae61-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ae61-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="3ae61-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ae61-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ae61-108">DESCRIPTION</span></span>
<span data-ttu-id="3ae61-109">**Get-AzStorageBlobServiceProperty** cmdlet 'ı, Azure depolama blob Hizmetleri için hizmet özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ae61-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="3ae61-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ae61-110">EXAMPLES</span></span>

### <span data-ttu-id="3ae61-111">Örnek 1: belirtilen depolama hesabının Azure depolama blob Hizmetleri özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="3ae61-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="3ae61-112">Bu komut, belirtilen depolama hesabının blob Hizmetleri özelliğini alır.</span><span class="sxs-lookup"><span data-stu-id="3ae61-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="3ae61-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ae61-113">PARAMETERS</span></span>

### <span data-ttu-id="3ae61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae61-114">-DefaultProfile</span></span>
<span data-ttu-id="3ae61-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ae61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae61-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae61-116">-ResourceGroupName</span></span>
<span data-ttu-id="3ae61-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3ae61-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="3ae61-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3ae61-118">-ResourceId</span></span>
<span data-ttu-id="3ae61-119">Blob hizmeti özellikleri kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3ae61-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="3ae61-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ae61-120">-StorageAccount</span></span>
<span data-ttu-id="3ae61-121">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3ae61-121">Storage account object</span></span>

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

### <span data-ttu-id="3ae61-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3ae61-122">-StorageAccountName</span></span>
<span data-ttu-id="3ae61-123">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="3ae61-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="3ae61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae61-124">CommonParameters</span></span>
<span data-ttu-id="3ae61-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ae61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae61-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae61-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ae61-127">INPUTS</span></span>

### <span data-ttu-id="3ae61-128">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ae61-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3ae61-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3ae61-129">System.String</span></span>

## <span data-ttu-id="3ae61-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ae61-130">OUTPUTS</span></span>

### <span data-ttu-id="3ae61-131">Microsoft. Azure. Commands. Management. Storage. model. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="3ae61-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="3ae61-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ae61-132">NOTES</span></span>

## <span data-ttu-id="3ae61-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ae61-133">RELATED LINKS</span></span>
