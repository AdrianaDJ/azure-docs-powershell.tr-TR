---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d5d43a0aebcc553a230655d52399081548aae209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763909"
---
# <span data-ttu-id="f06b2-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="f06b2-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="f06b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f06b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f06b2-103">Kayıt hesapları alın.</span><span class="sxs-lookup"><span data-stu-id="f06b2-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f06b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f06b2-104">SYNTAX</span></span>

### <span data-ttu-id="f06b2-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f06b2-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f06b2-106">Başına</span><span class="sxs-lookup"><span data-stu-id="f06b2-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f06b2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f06b2-107">DESCRIPTION</span></span>
<span data-ttu-id="f06b2-108">**Get-AzureRmEnrollmentAccount** cmdlet 'i kaydolma hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="f06b2-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="f06b2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f06b2-109">EXAMPLES</span></span>

### <span data-ttu-id="f06b2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f06b2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="f06b2-111">Tüm kullanılabilir kayıt hesaplarını edinin.</span><span class="sxs-lookup"><span data-stu-id="f06b2-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="f06b2-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f06b2-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="f06b2-113">Belirtilen nesne kimliğine sahip kayıt hesabını edinin.</span><span class="sxs-lookup"><span data-stu-id="f06b2-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="f06b2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f06b2-114">PARAMETERS</span></span>

### <span data-ttu-id="f06b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06b2-115">-DefaultProfile</span></span>
<span data-ttu-id="f06b2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f06b2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f06b2-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f06b2-117">-ObjectId</span></span>
<span data-ttu-id="f06b2-118">Belirli bir kayıt hesabının ObjectID.</span><span class="sxs-lookup"><span data-stu-id="f06b2-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="f06b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06b2-119">CommonParameters</span></span>
<span data-ttu-id="f06b2-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f06b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06b2-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f06b2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06b2-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f06b2-122">INPUTS</span></span>

### <span data-ttu-id="f06b2-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f06b2-123">None</span></span>

## <span data-ttu-id="f06b2-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f06b2-124">OUTPUTS</span></span>

### <span data-ttu-id="f06b2-125">Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem</span><span class="sxs-lookup"><span data-stu-id="f06b2-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="f06b2-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f06b2-126">NOTES</span></span>

## <span data-ttu-id="f06b2-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f06b2-127">RELATED LINKS</span></span>
