---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753134"
---
# <span data-ttu-id="5943a-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="5943a-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="5943a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5943a-102">SYNOPSIS</span></span>
<span data-ttu-id="5943a-103">Kayıt hesapları alın.</span><span class="sxs-lookup"><span data-stu-id="5943a-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="5943a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5943a-104">SYNTAX</span></span>

### <span data-ttu-id="5943a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5943a-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5943a-106">Başına</span><span class="sxs-lookup"><span data-stu-id="5943a-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5943a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5943a-107">DESCRIPTION</span></span>
<span data-ttu-id="5943a-108">**Get-Azte Mentaccount** cmdlet 'i kayıt hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="5943a-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="5943a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5943a-109">EXAMPLES</span></span>

### <span data-ttu-id="5943a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5943a-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="5943a-111">Tüm kullanılabilir kayıt hesaplarını edinin.</span><span class="sxs-lookup"><span data-stu-id="5943a-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="5943a-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5943a-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="5943a-113">Belirtilen nesne kimliğine sahip kayıt hesabını edinin.</span><span class="sxs-lookup"><span data-stu-id="5943a-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="5943a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5943a-114">PARAMETERS</span></span>

### <span data-ttu-id="5943a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5943a-115">-DefaultProfile</span></span>
<span data-ttu-id="5943a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5943a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5943a-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="5943a-117">-ObjectId</span></span>
<span data-ttu-id="5943a-118">Belirli bir kayıt hesabının ObjectID.</span><span class="sxs-lookup"><span data-stu-id="5943a-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5943a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5943a-119">CommonParameters</span></span>
<span data-ttu-id="5943a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5943a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5943a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5943a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5943a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5943a-122">INPUTS</span></span>

### <span data-ttu-id="5943a-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5943a-123">None</span></span>

## <span data-ttu-id="5943a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5943a-124">OUTPUTS</span></span>

### <span data-ttu-id="5943a-125">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="5943a-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="5943a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5943a-126">NOTES</span></span>

## <span data-ttu-id="5943a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5943a-127">RELATED LINKS</span></span>
