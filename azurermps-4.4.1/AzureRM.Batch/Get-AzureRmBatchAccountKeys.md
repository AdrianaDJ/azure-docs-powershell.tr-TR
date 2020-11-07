---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 6bab9613a2b109ef0cd8d0d65bf2fb770d91eb16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764082"
---
# <span data-ttu-id="651d1-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="651d1-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="651d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="651d1-102">SYNOPSIS</span></span>
<span data-ttu-id="651d1-103">Bir toplu Iş hesabındaki anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="651d1-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="651d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="651d1-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="651d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="651d1-105">DESCRIPTION</span></span>
<span data-ttu-id="651d1-106">**Get-AzureRmBatchAccountKeys** cmdlet 'i geçerli abonelikteki bir Azure toplu hesabının anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="651d1-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="651d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="651d1-107">EXAMPLES</span></span>

## <span data-ttu-id="651d1-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="651d1-108">PARAMETERS</span></span>

### <span data-ttu-id="651d1-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="651d1-109">-AccountName</span></span>
<span data-ttu-id="651d1-110">Bu cmdlet 'in anahtarları aldığı hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="651d1-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="651d1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651d1-111">-ResourceGroupName</span></span>
<span data-ttu-id="651d1-112">Bu cmdlet 'in anahtarları aldığı hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="651d1-112">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="651d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651d1-113">-DefaultProfile</span></span>
<span data-ttu-id="651d1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="651d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="651d1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651d1-115">CommonParameters</span></span>
<span data-ttu-id="651d1-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="651d1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651d1-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651d1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651d1-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="651d1-118">INPUTS</span></span>

## <span data-ttu-id="651d1-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="651d1-119">OUTPUTS</span></span>

### <span data-ttu-id="651d1-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="651d1-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="651d1-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="651d1-121">NOTES</span></span>

## <span data-ttu-id="651d1-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="651d1-122">RELATED LINKS</span></span>

[<span data-ttu-id="651d1-123">Yeni-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="651d1-123">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="651d1-124">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="651d1-124">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


