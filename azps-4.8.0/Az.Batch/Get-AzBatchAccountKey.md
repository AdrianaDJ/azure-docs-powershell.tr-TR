---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110072"
---
# <span data-ttu-id="45bd6-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="45bd6-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="45bd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="45bd6-103">Bir toplu Iş hesabındaki anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="45bd6-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="45bd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45bd6-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45bd6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="45bd6-106">**Get-AzBatchAccountKey** cmdlet 'i geçerli abonelikteki bir Azure toplu hesabının anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45bd6-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="45bd6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45bd6-107">EXAMPLES</span></span>

### <span data-ttu-id="45bd6-108">Örnek 1: toplu hesap anahtarlarını alın ve daha sonra kullanmak üzere $Context değişkenine kaydedin</span><span class="sxs-lookup"><span data-stu-id="45bd6-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="45bd6-109">Bu komut, hesap ayrıntılarını alır ve `$Context` daha sonra kullanmak üzere bir nesnede depolar.</span><span class="sxs-lookup"><span data-stu-id="45bd6-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="45bd6-110">Örnek 2: toplu hesap anahtarlarını alma ve görüntüleme</span><span class="sxs-lookup"><span data-stu-id="45bd6-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="45bd6-111">Bu komut hesap anahtarlarını alır ve konsola yazdırır.</span><span class="sxs-lookup"><span data-stu-id="45bd6-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="45bd6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45bd6-112">PARAMETERS</span></span>

### <span data-ttu-id="45bd6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="45bd6-113">-AccountName</span></span>
<span data-ttu-id="45bd6-114">Bu cmdlet 'in anahtarları aldığı hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45bd6-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="45bd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bd6-115">-DefaultProfile</span></span>
<span data-ttu-id="45bd6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45bd6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45bd6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bd6-117">-ResourceGroupName</span></span>
<span data-ttu-id="45bd6-118">Bu cmdlet 'in anahtarları aldığı hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45bd6-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="45bd6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bd6-119">CommonParameters</span></span>
<span data-ttu-id="45bd6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45bd6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bd6-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45bd6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bd6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45bd6-122">INPUTS</span></span>

### <span data-ttu-id="45bd6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="45bd6-123">System.String</span></span>

## <span data-ttu-id="45bd6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45bd6-124">OUTPUTS</span></span>

### <span data-ttu-id="45bd6-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="45bd6-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="45bd6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45bd6-126">NOTES</span></span>

## <span data-ttu-id="45bd6-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45bd6-127">RELATED LINKS</span></span>

[<span data-ttu-id="45bd6-128">Yeni-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="45bd6-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="45bd6-129">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="45bd6-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
