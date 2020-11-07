---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: 1ef273329634e080c4117b9ddd0d1eaf8d91bb0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765023"
---
# <span data-ttu-id="be00b-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="be00b-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="be00b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be00b-102">SYNOPSIS</span></span>
<span data-ttu-id="be00b-103">Geçerli aboneliğin depolama kaynağı kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="be00b-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be00b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be00b-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be00b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be00b-105">DESCRIPTION</span></span>
<span data-ttu-id="be00b-106">**Get-AzureRmStorageUsage** cmdlet 'i geçerli aboneliğin Azure depolama alanı için kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="be00b-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="be00b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be00b-107">EXAMPLES</span></span>

### <span data-ttu-id="be00b-108">Örnek 1: depolama kaynaklarının kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="be00b-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="be00b-109">Bu komut, geçerli aboneliğin depolama kaynakları kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="be00b-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="be00b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be00b-110">PARAMETERS</span></span>

### <span data-ttu-id="be00b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be00b-111">-DefaultProfile</span></span>
<span data-ttu-id="be00b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be00b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be00b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be00b-113">CommonParameters</span></span>
<span data-ttu-id="be00b-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be00b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be00b-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be00b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be00b-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be00b-116">INPUTS</span></span>

## <span data-ttu-id="be00b-117">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be00b-117">OUTPUTS</span></span>

## <span data-ttu-id="be00b-118">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be00b-118">NOTES</span></span>

## <span data-ttu-id="be00b-119">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be00b-119">RELATED LINKS</span></span>

[<span data-ttu-id="be00b-120">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="be00b-120">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)

