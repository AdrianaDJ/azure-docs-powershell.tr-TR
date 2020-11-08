---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278420"
---
# <span data-ttu-id="7fd68-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="7fd68-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="7fd68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd68-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd68-103">Kayıt hesapları alın.</span><span class="sxs-lookup"><span data-stu-id="7fd68-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="7fd68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fd68-104">SYNTAX</span></span>

### <span data-ttu-id="7fd68-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7fd68-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fd68-106">Başına</span><span class="sxs-lookup"><span data-stu-id="7fd68-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fd68-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fd68-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd68-108">**Get-Azte Mentaccount** cmdlet 'i kayıt hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="7fd68-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="7fd68-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fd68-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd68-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7fd68-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="7fd68-111">Tüm kullanılabilir kayıt hesaplarını edinin.</span><span class="sxs-lookup"><span data-stu-id="7fd68-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="7fd68-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7fd68-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="7fd68-113">Belirtilen nesne kimliğine sahip kayıt hesabını edinin.</span><span class="sxs-lookup"><span data-stu-id="7fd68-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="7fd68-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fd68-114">PARAMETERS</span></span>

### <span data-ttu-id="7fd68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd68-115">-DefaultProfile</span></span>
<span data-ttu-id="7fd68-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7fd68-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fd68-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7fd68-117">-ObjectId</span></span>
<span data-ttu-id="7fd68-118">Belirli bir kayıt hesabının ObjectID.</span><span class="sxs-lookup"><span data-stu-id="7fd68-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="7fd68-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd68-119">CommonParameters</span></span>
<span data-ttu-id="7fd68-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fd68-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd68-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd68-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd68-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fd68-122">INPUTS</span></span>

### <span data-ttu-id="7fd68-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7fd68-123">None</span></span>

## <span data-ttu-id="7fd68-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fd68-124">OUTPUTS</span></span>

### <span data-ttu-id="7fd68-125">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="7fd68-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="7fd68-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fd68-126">NOTES</span></span>

## <span data-ttu-id="7fd68-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fd68-127">RELATED LINKS</span></span>
