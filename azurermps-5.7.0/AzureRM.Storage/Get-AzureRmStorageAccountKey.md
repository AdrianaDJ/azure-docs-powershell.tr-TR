---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587402"
---
# <span data-ttu-id="b306d-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b306d-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="b306d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b306d-102">SYNOPSIS</span></span>
<span data-ttu-id="b306d-103">Azure depolama hesabı için erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b306d-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b306d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b306d-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="b306d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b306d-105">DESCRIPTION</span></span>
<span data-ttu-id="b306d-106">**Get-AzureRmStorageAccountKey** cmdlet 'ı bir Azure depolama hesabının erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b306d-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="b306d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b306d-107">EXAMPLES</span></span>

### <span data-ttu-id="b306d-108">Örnek 1: depolama hesabının erişim anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="b306d-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="b306d-109">Bu komut belirtilen Azure depolama hesabı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="b306d-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="b306d-110">Örnek 2: depolama hesabı için belirli bir erişim anahtarı alma</span><span class="sxs-lookup"><span data-stu-id="b306d-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="b306d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b306d-111">PARAMETERS</span></span>

### <span data-ttu-id="b306d-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="b306d-112">-Name</span></span>
<span data-ttu-id="b306d-113">Bu cmdlet 'in anahtarları aldığı depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b306d-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b306d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b306d-114">-ResourceGroupName</span></span>
<span data-ttu-id="b306d-115">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b306d-115">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b306d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b306d-116">CommonParameters</span></span>
<span data-ttu-id="b306d-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b306d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b306d-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b306d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b306d-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b306d-119">INPUTS</span></span>

### <span data-ttu-id="b306d-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b306d-120">None</span></span>
<span data-ttu-id="b306d-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b306d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b306d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b306d-122">OUTPUTS</span></span>

## <span data-ttu-id="b306d-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b306d-123">NOTES</span></span>

## <span data-ttu-id="b306d-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b306d-124">RELATED LINKS</span></span>

[<span data-ttu-id="b306d-125">Yeni-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b306d-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)
