---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 48de3ae521f77c531433ffca67dadc9e2c46a980
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593312"
---
# <span data-ttu-id="5f88f-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5f88f-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="5f88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f88f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f88f-103">Toplu hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5f88f-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f88f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f88f-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f88f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f88f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f88f-106">**Yeni-AzureRmBatchAccountKey** cmdlet 'ı bir Azure toplu hesabının birincil veya ikincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5f88f-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="5f88f-107">Cmdlet, geçerli bir sın **Yaccountkey** ve **SecondaryAccountKey** özelliklerine sahip bir **batchaccountcontext** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5f88f-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="5f88f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f88f-108">EXAMPLES</span></span>

### <span data-ttu-id="5f88f-109">Örnek 1: bir toplu Iş hesabında birincil hesap anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="5f88f-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="5f88f-110">Bu komut, pfuller adlı toplu Iş hesabındaki birincil hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5f88f-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="5f88f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f88f-111">PARAMETERS</span></span>

### <span data-ttu-id="5f88f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5f88f-112">-AccountName</span></span>
<span data-ttu-id="5f88f-113">Bu cmdlet 'in bir anahtarı yeniden sunduğu toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f88f-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="5f88f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f88f-114">-DefaultProfile</span></span>
<span data-ttu-id="5f88f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f88f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f88f-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5f88f-116">-KeyType</span></span>
<span data-ttu-id="5f88f-117">Bu cmdlet 'in yeniden kullandığı anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f88f-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="5f88f-118">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="5f88f-118">Valid values are:</span></span> 
- <span data-ttu-id="5f88f-119">Yararı</span><span class="sxs-lookup"><span data-stu-id="5f88f-119">Primary</span></span>
- <span data-ttu-id="5f88f-120">İK</span><span class="sxs-lookup"><span data-stu-id="5f88f-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f88f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f88f-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f88f-122">Bu cmdlet 'in bir anahtarı yeniden sunduğu hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f88f-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="5f88f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f88f-123">CommonParameters</span></span>
<span data-ttu-id="5f88f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f88f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f88f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f88f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f88f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f88f-126">INPUTS</span></span>

### <span data-ttu-id="5f88f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5f88f-127">System.String</span></span>

## <span data-ttu-id="5f88f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f88f-128">OUTPUTS</span></span>

### <span data-ttu-id="5f88f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5f88f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5f88f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f88f-130">NOTES</span></span>

## <span data-ttu-id="5f88f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f88f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f88f-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5f88f-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5f88f-133">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5f88f-133">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


