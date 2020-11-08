---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: c0b283c7645426af9397fd675fde825ff0b5f087
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279759"
---
# <span data-ttu-id="174e5-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="174e5-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="174e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="174e5-102">SYNOPSIS</span></span>
<span data-ttu-id="174e5-103">Depolama hesap adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="174e5-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="174e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="174e5-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="174e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="174e5-105">DESCRIPTION</span></span>
<span data-ttu-id="174e5-106">**Get-Azstorageaccountnameuygunluk** cmdlet 'ı, Azure depolama hesabı adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="174e5-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="174e5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="174e5-107">EXAMPLES</span></span>

### <span data-ttu-id="174e5-108">Örnek 1: depolama hesap adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="174e5-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="174e5-109">Bu komut, ContosoStorage03 adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="174e5-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="174e5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="174e5-110">PARAMETERS</span></span>

### <span data-ttu-id="174e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174e5-111">-DefaultProfile</span></span>
<span data-ttu-id="174e5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="174e5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="174e5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="174e5-113">-Name</span></span>
<span data-ttu-id="174e5-114">Bu cmdlet 'in denetlediği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="174e5-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="174e5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174e5-115">CommonParameters</span></span>
<span data-ttu-id="174e5-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="174e5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174e5-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174e5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174e5-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="174e5-118">INPUTS</span></span>

### <span data-ttu-id="174e5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="174e5-119">System.String</span></span>

## <span data-ttu-id="174e5-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="174e5-120">OUTPUTS</span></span>

### <span data-ttu-id="174e5-121">Microsoft. Azure. Management. Storage. model. Checknamekullanılabilirliği Bilityresult</span><span class="sxs-lookup"><span data-stu-id="174e5-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="174e5-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="174e5-122">NOTES</span></span>

## <span data-ttu-id="174e5-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="174e5-123">RELATED LINKS</span></span>

[<span data-ttu-id="174e5-124">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="174e5-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


