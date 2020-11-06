---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591281"
---
# <span data-ttu-id="6fe71-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6fe71-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="6fe71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe71-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe71-103">Geçerli aboneliğin depolama kaynağı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="6fe71-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fe71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fe71-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fe71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fe71-105">DESCRIPTION</span></span>
<span data-ttu-id="6fe71-106">**Get-AzureRmStorageUsage** cmdlet 'i geçerli aboneliğin Azure depolama alanı için kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="6fe71-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="6fe71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fe71-107">EXAMPLES</span></span>

### <span data-ttu-id="6fe71-108">Örnek 1: depolama kaynaklarının kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="6fe71-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="6fe71-109">Bu komut, geçerli aboneliğin depolama kaynakları kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="6fe71-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="6fe71-110">Örnek 2: belirtilen konumun depolama kaynakları kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="6fe71-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="6fe71-111">Bu komut, geçerli aboneliğin altındaki belirtilen konumun depolama kaynakları kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="6fe71-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="6fe71-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fe71-112">PARAMETERS</span></span>

### <span data-ttu-id="6fe71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe71-113">-DefaultProfile</span></span>
<span data-ttu-id="6fe71-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fe71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe71-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="6fe71-115">-Location</span></span>
<span data-ttu-id="6fe71-116">Belirtilen konumda depolama kaynakları kullanımının alınacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="6fe71-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="6fe71-117">Belirtilmemişse, aboneliğin altındaki tüm konumlarda depolama kaynakları kullanımı elde edilir.</span><span class="sxs-lookup"><span data-stu-id="6fe71-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe71-118">CommonParameters</span></span>
<span data-ttu-id="6fe71-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fe71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe71-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe71-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe71-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fe71-121">INPUTS</span></span>

### <span data-ttu-id="6fe71-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6fe71-122">None</span></span>

## <span data-ttu-id="6fe71-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fe71-123">OUTPUTS</span></span>

### <span data-ttu-id="6fe71-124">Microsoft. Azure. Commands. Management. Storage. model. PSUsage</span><span class="sxs-lookup"><span data-stu-id="6fe71-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="6fe71-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fe71-125">NOTES</span></span>

## <span data-ttu-id="6fe71-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fe71-126">RELATED LINKS</span></span>

[<span data-ttu-id="6fe71-127">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6fe71-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


