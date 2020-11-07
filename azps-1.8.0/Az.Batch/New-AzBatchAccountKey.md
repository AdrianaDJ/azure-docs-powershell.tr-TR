---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: b766e0752afa60f8d9619aebd711653688566582
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761861"
---
# <span data-ttu-id="e4f7e-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4f7e-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="e4f7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f7e-103">Toplu hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="e4f7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4f7e-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4f7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f7e-106">**New-AzBatchAccountKey** cmdlet 'ı Azure toplu hesabının birincil veya ikincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="e4f7e-107">Cmdlet, geçerli bir sın **Yaccountkey** ve **SecondaryAccountKey** özelliklerine sahip bir **batchaccountcontext** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="e4f7e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4f7e-108">EXAMPLES</span></span>

### <span data-ttu-id="e4f7e-109">Örnek 1: bir toplu Iş hesabında birincil hesap anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4f7e-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="e4f7e-110">Bu komut, pfuller adlı toplu Iş hesabındaki birincil hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="e4f7e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4f7e-111">PARAMETERS</span></span>

### <span data-ttu-id="e4f7e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e4f7e-112">-AccountName</span></span>
<span data-ttu-id="e4f7e-113">Bu cmdlet 'in bir anahtarı yeniden sunduğu toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="e4f7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f7e-114">-DefaultProfile</span></span>
<span data-ttu-id="e4f7e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4f7e-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e4f7e-116">-KeyType</span></span>
<span data-ttu-id="e4f7e-117">Bu cmdlet 'in yeniden kullandığı anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="e4f7e-118">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e4f7e-118">Valid values are:</span></span> 
- <span data-ttu-id="e4f7e-119">Yararı</span><span class="sxs-lookup"><span data-stu-id="e4f7e-119">Primary</span></span>
- <span data-ttu-id="e4f7e-120">İK</span><span class="sxs-lookup"><span data-stu-id="e4f7e-120">Secondary</span></span>

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

### <span data-ttu-id="e4f7e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f7e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4f7e-122">Bu cmdlet 'in bir anahtarı yeniden sunduğu hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="e4f7e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f7e-123">CommonParameters</span></span>
<span data-ttu-id="e4f7e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4f7e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f7e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f7e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f7e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4f7e-126">INPUTS</span></span>

### <span data-ttu-id="e4f7e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e4f7e-127">System.String</span></span>

## <span data-ttu-id="e4f7e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4f7e-128">OUTPUTS</span></span>

### <span data-ttu-id="e4f7e-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e4f7e-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e4f7e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4f7e-130">NOTES</span></span>

## <span data-ttu-id="e4f7e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4f7e-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4f7e-132">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="e4f7e-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e4f7e-133">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e4f7e-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


