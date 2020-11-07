---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
ms.openlocfilehash: 5371b5c54cfaff4b1c48dd8a8643e0cc51b1e00e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939221"
---
# <span data-ttu-id="c0a74-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c0a74-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="c0a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0a74-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a74-103">Depolama hesap adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="c0a74-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0a74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0a74-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0a74-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0a74-105">DESCRIPTION</span></span>
<span data-ttu-id="c0a74-106">**Get-Azurermstorageaccountnameuygunluk** cmdlet 'ı, Azure depolama hesabı adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="c0a74-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="c0a74-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0a74-107">EXAMPLES</span></span>

### <span data-ttu-id="c0a74-108">Örnek 1: depolama hesap adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="c0a74-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="c0a74-109">Bu komut, ContosoStorage03 adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="c0a74-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="c0a74-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0a74-110">PARAMETERS</span></span>

### <span data-ttu-id="c0a74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a74-111">-DefaultProfile</span></span>
<span data-ttu-id="c0a74-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0a74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a74-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0a74-113">-Name</span></span>
<span data-ttu-id="c0a74-114">Bu cmdlet 'in denetlediği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0a74-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a74-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a74-115">CommonParameters</span></span>
<span data-ttu-id="c0a74-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0a74-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a74-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a74-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a74-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0a74-118">INPUTS</span></span>

### <span data-ttu-id="c0a74-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c0a74-119">System.String</span></span>

## <span data-ttu-id="c0a74-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0a74-120">OUTPUTS</span></span>

### <span data-ttu-id="c0a74-121">Microsoft. Azure. Management. Storage. model. Checknamekullanılabilirliği Bilityresult</span><span class="sxs-lookup"><span data-stu-id="c0a74-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="c0a74-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0a74-122">NOTES</span></span>

## <span data-ttu-id="c0a74-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0a74-123">RELATED LINKS</span></span>

[<span data-ttu-id="c0a74-124">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c0a74-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


