---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: ae6524c46ed97563e7bf6c948f550a393d74f582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939215"
---
# <span data-ttu-id="986cb-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="986cb-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="986cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986cb-102">SYNOPSIS</span></span>
<span data-ttu-id="986cb-103">Geçerli aboneliğin depolama kaynağı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="986cb-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="986cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="986cb-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="986cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="986cb-105">DESCRIPTION</span></span>
<span data-ttu-id="986cb-106">**Get-AzureRmStorageUsage** cmdlet 'i geçerli aboneliğin Azure depolama alanı için kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="986cb-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="986cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="986cb-107">EXAMPLES</span></span>

### <span data-ttu-id="986cb-108">Örnek 1: depolama kaynaklarının kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="986cb-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="986cb-109">Bu komut, geçerli aboneliğin depolama kaynakları kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="986cb-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="986cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="986cb-110">PARAMETERS</span></span>

### <span data-ttu-id="986cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986cb-111">-DefaultProfile</span></span>
<span data-ttu-id="986cb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="986cb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="986cb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986cb-113">CommonParameters</span></span>
<span data-ttu-id="986cb-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="986cb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986cb-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986cb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986cb-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="986cb-116">INPUTS</span></span>

### <span data-ttu-id="986cb-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="986cb-117">None</span></span>

## <span data-ttu-id="986cb-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="986cb-118">OUTPUTS</span></span>

### <span data-ttu-id="986cb-119">Microsoft. Azure. Commands. Management. Storage. model. PSUsage</span><span class="sxs-lookup"><span data-stu-id="986cb-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="986cb-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="986cb-120">NOTES</span></span>

## <span data-ttu-id="986cb-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="986cb-121">RELATED LINKS</span></span>

[<span data-ttu-id="986cb-122">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="986cb-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


