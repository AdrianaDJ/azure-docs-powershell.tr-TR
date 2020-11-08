---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: e079701f0d2ccca49e1368edc9446c08b4549c11
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107217"
---
# <span data-ttu-id="5eebf-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5eebf-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="5eebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eebf-102">SYNOPSIS</span></span>
<span data-ttu-id="5eebf-103">Toplu hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5eebf-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="5eebf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5eebf-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eebf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5eebf-105">DESCRIPTION</span></span>
<span data-ttu-id="5eebf-106">**New-AzBatchAccountKey** cmdlet 'ı Azure toplu hesabının birincil veya ikincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5eebf-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="5eebf-107">Cmdlet, geçerli bir sın **Yaccountkey** ve **SecondaryAccountKey** özelliklerine sahip bir **batchaccountcontext** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5eebf-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="5eebf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5eebf-108">EXAMPLES</span></span>

### <span data-ttu-id="5eebf-109">Örnek 1: bir toplu Iş hesabında birincil hesap anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="5eebf-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="5eebf-110">Bu komut, pfuller adlı toplu Iş hesabındaki birincil hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5eebf-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="5eebf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5eebf-111">PARAMETERS</span></span>

### <span data-ttu-id="5eebf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5eebf-112">-AccountName</span></span>
<span data-ttu-id="5eebf-113">Bu cmdlet 'in bir anahtarı yeniden sunduğu toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5eebf-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="5eebf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eebf-114">-DefaultProfile</span></span>
<span data-ttu-id="5eebf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5eebf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eebf-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5eebf-116">-KeyType</span></span>
<span data-ttu-id="5eebf-117">Bu cmdlet 'in yeniden kullandığı anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5eebf-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="5eebf-118">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="5eebf-118">Valid values are:</span></span> 
- <span data-ttu-id="5eebf-119">Yararı</span><span class="sxs-lookup"><span data-stu-id="5eebf-119">Primary</span></span>
- <span data-ttu-id="5eebf-120">İK</span><span class="sxs-lookup"><span data-stu-id="5eebf-120">Secondary</span></span>

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

### <span data-ttu-id="5eebf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eebf-121">-ResourceGroupName</span></span>
<span data-ttu-id="5eebf-122">Bu cmdlet 'in bir anahtarı yeniden sunduğu hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5eebf-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="5eebf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eebf-123">CommonParameters</span></span>
<span data-ttu-id="5eebf-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5eebf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eebf-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5eebf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eebf-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5eebf-126">INPUTS</span></span>

### <span data-ttu-id="5eebf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5eebf-127">System.String</span></span>

## <span data-ttu-id="5eebf-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5eebf-128">OUTPUTS</span></span>

### <span data-ttu-id="5eebf-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5eebf-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5eebf-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5eebf-130">NOTES</span></span>

## <span data-ttu-id="5eebf-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5eebf-131">RELATED LINKS</span></span>

[<span data-ttu-id="5eebf-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5eebf-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5eebf-133">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5eebf-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


