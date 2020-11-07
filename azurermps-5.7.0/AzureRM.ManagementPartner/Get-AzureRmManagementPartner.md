---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590995"
---
# <span data-ttu-id="0770c-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0770c-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="0770c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0770c-102">SYNOPSIS</span></span>
<span data-ttu-id="0770c-103">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="0770c-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0770c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0770c-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0770c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0770c-105">DESCRIPTION</span></span>
<span data-ttu-id="0770c-106">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="0770c-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="0770c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0770c-107">EXAMPLES</span></span>

### <span data-ttu-id="0770c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0770c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0770c-109">Geçerli yönetim ortağı kimliği</span><span class="sxs-lookup"><span data-stu-id="0770c-109">Get the current management partner id</span></span>

### <span data-ttu-id="0770c-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0770c-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0770c-111">Geçerli yönetim ortağı kimliği, bir iş ortağı kimliği ile eşleşmezse, eşleşmezse başarısız olur</span><span class="sxs-lookup"><span data-stu-id="0770c-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="0770c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0770c-112">PARAMETERS</span></span>

### <span data-ttu-id="0770c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0770c-113">-DefaultProfile</span></span>
<span data-ttu-id="0770c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0770c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0770c-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0770c-115">-PartnerId</span></span>
<span data-ttu-id="0770c-116">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="0770c-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0770c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0770c-117">CommonParameters</span></span>
<span data-ttu-id="0770c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0770c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0770c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0770c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0770c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0770c-120">INPUTS</span></span>

### <span data-ttu-id="0770c-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0770c-121">None</span></span>

## <span data-ttu-id="0770c-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0770c-122">OUTPUTS</span></span>

### <span data-ttu-id="0770c-123">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0770c-123">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="0770c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0770c-124">NOTES</span></span>

## <span data-ttu-id="0770c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0770c-125">RELATED LINKS</span></span>

[<span data-ttu-id="0770c-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0770c-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="0770c-127">Yeni-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0770c-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="0770c-128">Güncelleştirme-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0770c-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)