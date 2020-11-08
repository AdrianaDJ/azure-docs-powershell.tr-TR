---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 60e30de4d6d55007ec659a267b1d450ac1cfeff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934066"
---
# <span data-ttu-id="9bd8e-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9bd8e-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="9bd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd8e-103">Depolama hesap adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="9bd8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bd8e-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bd8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bd8e-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd8e-106">**Get-Azstorageaccountnameuygunluk** cmdlet 'ı, Azure depolama hesabı adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="9bd8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bd8e-107">EXAMPLES</span></span>

### <span data-ttu-id="9bd8e-108">Örnek 1: depolama hesap adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="9bd8e-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="9bd8e-109">Bu komut, ContosoStorage03 adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="9bd8e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bd8e-110">PARAMETERS</span></span>

### <span data-ttu-id="9bd8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd8e-111">-DefaultProfile</span></span>
<span data-ttu-id="9bd8e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd8e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bd8e-113">-Name</span></span>
<span data-ttu-id="9bd8e-114">Bu cmdlet 'in denetlediği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="9bd8e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd8e-115">CommonParameters</span></span>
<span data-ttu-id="9bd8e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd8e-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd8e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd8e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bd8e-118">INPUTS</span></span>

### <span data-ttu-id="9bd8e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9bd8e-119">System.String</span></span>

## <span data-ttu-id="9bd8e-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bd8e-120">OUTPUTS</span></span>

### <span data-ttu-id="9bd8e-121">Microsoft. Azure. Management. Storage. model. Checknamekullanılabilirliği Bilityresult</span><span class="sxs-lookup"><span data-stu-id="9bd8e-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="9bd8e-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bd8e-122">NOTES</span></span>

## <span data-ttu-id="9bd8e-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bd8e-123">RELATED LINKS</span></span>

[<span data-ttu-id="9bd8e-124">Azure Depolama Yöneticisi cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="9bd8e-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)

