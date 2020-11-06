---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587666"
---
# <span data-ttu-id="e8ac3-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="e8ac3-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="e8ac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ac3-103">Kayıt hesapları alın.</span><span class="sxs-lookup"><span data-stu-id="e8ac3-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8ac3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8ac3-104">SYNTAX</span></span>

### <span data-ttu-id="e8ac3-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8ac3-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ac3-106">Başına</span><span class="sxs-lookup"><span data-stu-id="e8ac3-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ac3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8ac3-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ac3-108">**Get-AzureRmEnrollmentAccount** cmdlet 'i kaydolma hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="e8ac3-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="e8ac3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8ac3-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ac3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8ac3-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="e8ac3-111">Tüm kullanılabilir kayıt hesaplarını edinin.</span><span class="sxs-lookup"><span data-stu-id="e8ac3-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="e8ac3-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e8ac3-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="e8ac3-113">Belirtilen nesne kimliğine sahip kayıt hesabını edinin.</span><span class="sxs-lookup"><span data-stu-id="e8ac3-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="e8ac3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8ac3-114">PARAMETERS</span></span>

### <span data-ttu-id="e8ac3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ac3-115">-DefaultProfile</span></span>
<span data-ttu-id="e8ac3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e8ac3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ac3-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e8ac3-117">-ObjectId</span></span>
<span data-ttu-id="e8ac3-118">Belirli bir kayıt hesabının ObjectID.</span><span class="sxs-lookup"><span data-stu-id="e8ac3-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ac3-119">CommonParameters</span></span>
<span data-ttu-id="e8ac3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8ac3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ac3-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ac3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ac3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8ac3-122">INPUTS</span></span>

### <span data-ttu-id="e8ac3-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e8ac3-123">None</span></span>

## <span data-ttu-id="e8ac3-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8ac3-124">OUTPUTS</span></span>

### <span data-ttu-id="e8ac3-125">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. faturalandırma. modeller. PSEnrollmentAccount, Microsoft. Azure. Commands. Faturalandırma, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e8ac3-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e8ac3-126">Microsoft. Azure. Commands. faturalandırma. modeller. PSEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="e8ac3-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="e8ac3-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8ac3-127">NOTES</span></span>

## <span data-ttu-id="e8ac3-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8ac3-128">RELATED LINKS</span></span>

