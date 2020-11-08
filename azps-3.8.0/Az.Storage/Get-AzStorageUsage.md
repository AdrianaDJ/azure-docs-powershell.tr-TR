---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097744"
---
# <span data-ttu-id="c05fe-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c05fe-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="c05fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c05fe-103">Geçerli aboneliğin depolama kaynağı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c05fe-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="c05fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c05fe-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c05fe-105">DESCRIPTION</span></span>
<span data-ttu-id="c05fe-106">**Get-AzStorageUsage** cmdlet 'i geçerli aboneliğin Azure depolama alanı için kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c05fe-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="c05fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c05fe-107">EXAMPLES</span></span>

### <span data-ttu-id="c05fe-108">Örnek 1: belirtilen konumun depolama kaynakları kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="c05fe-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="c05fe-109">Bu komut, geçerli aboneliğin altındaki belirtilen konumun depolama kaynakları kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c05fe-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="c05fe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c05fe-110">PARAMETERS</span></span>

### <span data-ttu-id="c05fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05fe-111">-DefaultProfile</span></span>
<span data-ttu-id="c05fe-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c05fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c05fe-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="c05fe-113">-Location</span></span>
<span data-ttu-id="c05fe-114">Belirtilen konumda depolama kaynakları kullanımının alınacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c05fe-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="c05fe-115">Belirtilmemişse, aboneliğin altındaki tüm konumlarda depolama kaynakları kullanımı elde edilir.</span><span class="sxs-lookup"><span data-stu-id="c05fe-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05fe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05fe-116">CommonParameters</span></span>
<span data-ttu-id="c05fe-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c05fe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05fe-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05fe-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05fe-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c05fe-119">INPUTS</span></span>

### <span data-ttu-id="c05fe-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c05fe-120">System.String</span></span>

## <span data-ttu-id="c05fe-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c05fe-121">OUTPUTS</span></span>

### <span data-ttu-id="c05fe-122">Microsoft. Azure. Commands. Management. Storage. model. PSUsage</span><span class="sxs-lookup"><span data-stu-id="c05fe-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="c05fe-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c05fe-123">NOTES</span></span>

## <span data-ttu-id="c05fe-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c05fe-124">RELATED LINKS</span></span>

[<span data-ttu-id="c05fe-125">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c05fe-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)

