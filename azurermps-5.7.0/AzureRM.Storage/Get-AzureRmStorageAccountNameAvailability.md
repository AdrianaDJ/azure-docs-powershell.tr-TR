---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762137"
---
# <span data-ttu-id="308dc-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="308dc-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="308dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308dc-102">SYNOPSIS</span></span>
<span data-ttu-id="308dc-103">Depolama hesap adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="308dc-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="308dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="308dc-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="308dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="308dc-105">DESCRIPTION</span></span>
<span data-ttu-id="308dc-106">**Get-Azurermstorageaccountnameuygunluk** cmdlet 'ı, Azure depolama hesabı adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="308dc-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="308dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="308dc-107">EXAMPLES</span></span>

### <span data-ttu-id="308dc-108">Örnek 1: depolama hesap adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="308dc-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="308dc-109">Bu komut, ContosoStorage03 adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="308dc-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="308dc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="308dc-110">PARAMETERS</span></span>

### <span data-ttu-id="308dc-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="308dc-111">-Name</span></span>
<span data-ttu-id="308dc-112">Bu cmdlet 'in denetlediği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="308dc-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="308dc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308dc-113">CommonParameters</span></span>
<span data-ttu-id="308dc-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="308dc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308dc-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308dc-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308dc-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="308dc-116">INPUTS</span></span>

### <span data-ttu-id="308dc-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="308dc-117">None</span></span>
<span data-ttu-id="308dc-118">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="308dc-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="308dc-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="308dc-119">OUTPUTS</span></span>

## <span data-ttu-id="308dc-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="308dc-120">NOTES</span></span>

## <span data-ttu-id="308dc-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="308dc-121">RELATED LINKS</span></span>

[<span data-ttu-id="308dc-122">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="308dc-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)
