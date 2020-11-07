---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936239"
---
# <span data-ttu-id="c6a8a-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c6a8a-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="c6a8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a8a-103">Geçerli aboneliğin depolama kaynağı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c6a8a-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="c6a8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6a8a-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a8a-106">**Get-AzStorageUsage** cmdlet 'i geçerli aboneliğin Azure depolama alanı için kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c6a8a-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="c6a8a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6a8a-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a8a-108">Örnek 1: depolama kaynaklarının kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="c6a8a-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="c6a8a-109">Bu komut, geçerli aboneliğin depolama kaynakları kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="c6a8a-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="c6a8a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6a8a-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a8a-111">-DefaultProfile</span></span>
<span data-ttu-id="c6a8a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6a8a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a8a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a8a-113">CommonParameters</span></span>
<span data-ttu-id="c6a8a-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6a8a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a8a-115">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a8a-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a8a-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6a8a-116">INPUTS</span></span>

### <span data-ttu-id="c6a8a-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c6a8a-117">None</span></span>

## <span data-ttu-id="c6a8a-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6a8a-118">OUTPUTS</span></span>

### <span data-ttu-id="c6a8a-119">Microsoft. Azure. Commands. Management. Storage. model. PSUsage</span><span class="sxs-lookup"><span data-stu-id="c6a8a-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="c6a8a-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6a8a-120">NOTES</span></span>

## <span data-ttu-id="c6a8a-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6a8a-121">RELATED LINKS</span></span>

[<span data-ttu-id="c6a8a-122">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c6a8a-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


