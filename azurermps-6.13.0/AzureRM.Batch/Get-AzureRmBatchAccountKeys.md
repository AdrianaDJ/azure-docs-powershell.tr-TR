---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 1f32e700cd5d0c20e041143e43755172ecf2da86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593313"
---
# <span data-ttu-id="3b5b4-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3b5b4-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="3b5b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5b4-103">Bir toplu Iş hesabındaki anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="3b5b4-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b5b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b5b4-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b5b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b5b4-105">DESCRIPTION</span></span>
<span data-ttu-id="3b5b4-106">**Get-AzureRmBatchAccountKeys** cmdlet 'i geçerli abonelikteki bir Azure toplu hesabının anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3b5b4-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="3b5b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b5b4-107">EXAMPLES</span></span>

## <span data-ttu-id="3b5b4-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b5b4-108">PARAMETERS</span></span>

### <span data-ttu-id="3b5b4-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b5b4-109">-AccountName</span></span>
<span data-ttu-id="3b5b4-110">Bu cmdlet 'in anahtarları aldığı hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b5b4-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="3b5b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5b4-111">-DefaultProfile</span></span>
<span data-ttu-id="3b5b4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b5b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b5b4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5b4-113">-ResourceGroupName</span></span>
<span data-ttu-id="3b5b4-114">Bu cmdlet 'in anahtarları aldığı hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b5b4-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="3b5b4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5b4-115">CommonParameters</span></span>
<span data-ttu-id="3b5b4-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b5b4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5b4-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5b4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5b4-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b5b4-118">INPUTS</span></span>

### <span data-ttu-id="3b5b4-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3b5b4-119">System.String</span></span>

## <span data-ttu-id="3b5b4-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b5b4-120">OUTPUTS</span></span>

### <span data-ttu-id="3b5b4-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3b5b4-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3b5b4-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b5b4-122">NOTES</span></span>

## <span data-ttu-id="3b5b4-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b5b4-123">RELATED LINKS</span></span>

[<span data-ttu-id="3b5b4-124">Yeni-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3b5b4-124">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="3b5b4-125">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="3b5b4-125">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


