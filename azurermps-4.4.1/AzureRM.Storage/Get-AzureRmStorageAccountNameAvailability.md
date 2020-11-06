---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8ca5c33944882fde7e9bad2411df5f41dbe5f788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589943"
---
# <span data-ttu-id="e53ce-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e53ce-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="e53ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e53ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e53ce-103">Depolama hesap adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="e53ce-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e53ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e53ce-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e53ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e53ce-105">DESCRIPTION</span></span>
<span data-ttu-id="e53ce-106">**Get-Azurermstorageaccountnameuygunluk** cmdlet 'ı, Azure depolama hesabı adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="e53ce-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="e53ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e53ce-107">EXAMPLES</span></span>

### <span data-ttu-id="e53ce-108">Örnek 1: depolama hesap adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="e53ce-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="e53ce-109">Bu komut, ContosoStorage03 adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="e53ce-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="e53ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e53ce-110">PARAMETERS</span></span>

### <span data-ttu-id="e53ce-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="e53ce-111">-Name</span></span>
<span data-ttu-id="e53ce-112">Bu cmdlet 'in denetlediği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e53ce-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="e53ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53ce-113">-DefaultProfile</span></span>
<span data-ttu-id="e53ce-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e53ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e53ce-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53ce-115">CommonParameters</span></span>
<span data-ttu-id="e53ce-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e53ce-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53ce-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e53ce-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53ce-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e53ce-118">INPUTS</span></span>

## <span data-ttu-id="e53ce-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e53ce-119">OUTPUTS</span></span>

## <span data-ttu-id="e53ce-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e53ce-120">NOTES</span></span>

## <span data-ttu-id="e53ce-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e53ce-121">RELATED LINKS</span></span>

[<span data-ttu-id="e53ce-122">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e53ce-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


