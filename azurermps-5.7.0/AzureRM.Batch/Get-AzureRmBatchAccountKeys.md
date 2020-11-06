---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586818"
---
# <span data-ttu-id="03666-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="03666-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="03666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03666-102">SYNOPSIS</span></span>
<span data-ttu-id="03666-103">Bir toplu Iş hesabındaki anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="03666-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03666-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03666-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03666-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03666-105">DESCRIPTION</span></span>
<span data-ttu-id="03666-106">**Get-AzureRmBatchAccountKeys** cmdlet 'i geçerli abonelikteki bir Azure toplu hesabının anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="03666-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="03666-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03666-107">EXAMPLES</span></span>

## <span data-ttu-id="03666-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03666-108">PARAMETERS</span></span>

### <span data-ttu-id="03666-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="03666-109">-AccountName</span></span>
<span data-ttu-id="03666-110">Bu cmdlet 'in anahtarları aldığı hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03666-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03666-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03666-111">-DefaultProfile</span></span>
<span data-ttu-id="03666-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03666-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03666-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03666-113">-ResourceGroupName</span></span>
<span data-ttu-id="03666-114">Bu cmdlet 'in anahtarları aldığı hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03666-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03666-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03666-115">CommonParameters</span></span>
<span data-ttu-id="03666-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03666-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03666-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03666-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03666-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03666-118">INPUTS</span></span>

### <span data-ttu-id="03666-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="03666-119">None</span></span>
<span data-ttu-id="03666-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="03666-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03666-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03666-121">OUTPUTS</span></span>

### <span data-ttu-id="03666-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="03666-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="03666-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03666-123">NOTES</span></span>

## <span data-ttu-id="03666-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03666-124">RELATED LINKS</span></span>

[<span data-ttu-id="03666-125">Yeni-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="03666-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="03666-126">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="03666-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


