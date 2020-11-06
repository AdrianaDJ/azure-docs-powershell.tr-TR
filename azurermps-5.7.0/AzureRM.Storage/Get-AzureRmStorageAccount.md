---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587404"
---
# <span data-ttu-id="f289f-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f289f-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="f289f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f289f-102">SYNOPSIS</span></span>
<span data-ttu-id="f289f-103">Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="f289f-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f289f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f289f-104">SYNTAX</span></span>

### <span data-ttu-id="f289f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f289f-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="f289f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f289f-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="f289f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f289f-107">DESCRIPTION</span></span>
<span data-ttu-id="f289f-108">**Get-AzureRmStorageAccount** cmdlet 'i, belirli bir depolama hesabını veya bir kaynak grubundaki veya abonelikteki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="f289f-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="f289f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f289f-109">EXAMPLES</span></span>

### <span data-ttu-id="f289f-110">Örnek 1: belirtilen depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="f289f-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="f289f-111">Bu komut belirtilen depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="f289f-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="f289f-112">Örnek 2: kaynak grubundaki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="f289f-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="f289f-113">Bu komut, kaynak grubundaki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="f289f-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="f289f-114">Örnek 3: abonelikteki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="f289f-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="f289f-115">Bu komut, abonelikteki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="f289f-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="f289f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f289f-116">PARAMETERS</span></span>

### <span data-ttu-id="f289f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f289f-117">-Name</span></span>
<span data-ttu-id="f289f-118">Alınacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f289f-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f289f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f289f-119">-ResourceGroupName</span></span>
<span data-ttu-id="f289f-120">Alınacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f289f-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f289f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f289f-121">CommonParameters</span></span>
<span data-ttu-id="f289f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f289f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f289f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f289f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f289f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f289f-124">INPUTS</span></span>

### <span data-ttu-id="f289f-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f289f-125">None</span></span>
<span data-ttu-id="f289f-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f289f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f289f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f289f-127">OUTPUTS</span></span>

## <span data-ttu-id="f289f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f289f-128">NOTES</span></span>

## <span data-ttu-id="f289f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f289f-129">RELATED LINKS</span></span>

[<span data-ttu-id="f289f-130">Yeni-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f289f-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="f289f-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f289f-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="f289f-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f289f-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
