---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323953"
---
# <span data-ttu-id="a9017-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="a9017-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="a9017-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9017-102">SYNOPSIS</span></span>
<span data-ttu-id="a9017-103">Fatura hesapları edinin.</span><span class="sxs-lookup"><span data-stu-id="a9017-103">Get billing accounts.</span></span>

## <span data-ttu-id="a9017-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9017-104">SYNTAX</span></span>

### <span data-ttu-id="a9017-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9017-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9017-106">Başına</span><span class="sxs-lookup"><span data-stu-id="a9017-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9017-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9017-107">DESCRIPTION</span></span>
<span data-ttu-id="a9017-108">**Get-AzBillingAccount** cmdlet 'i fatura hesaplarını alır, kullanıcının erişimi olur.</span><span class="sxs-lookup"><span data-stu-id="a9017-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="a9017-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9017-109">EXAMPLES</span></span>

### <span data-ttu-id="a9017-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9017-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="a9017-111">Kullanıcının erişebileceği tüm ödeme hesaplarını edinin.</span><span class="sxs-lookup"><span data-stu-id="a9017-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="a9017-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a9017-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a9017-113">Belirtilen adla faturalandırma hesabı alın.</span><span class="sxs-lookup"><span data-stu-id="a9017-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="a9017-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a9017-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="a9017-115">Tüm faturalama hesaplarının kullanıcısına erişimi alın ve adresi sonuca ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="a9017-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a9017-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="a9017-117">Tüm faturalama hesaplarının kullanıcısına erişimi alın ve sonuç olarak faturalandırma profillerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="a9017-118">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="a9017-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="a9017-119">Tüm faturalandırma hesaplarının kullanıcısına erişimi olan tüm fatura hesaplarını alın ve sonuç olarak bunların altında faturalandırma profilleri ve fatura bölümlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="a9017-120">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="a9017-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a9017-121">Belirtilen adı taşıyan faturalandırma hesabını alın ve adres, faturalandırma profilleri ve fatura bölümlerini sonuçlarda ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="a9017-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9017-122">PARAMETERS</span></span>

### <span data-ttu-id="a9017-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9017-123">-DefaultProfile</span></span>
<span data-ttu-id="a9017-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a9017-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9017-125">-Includeaddress</span><span class="sxs-lookup"><span data-stu-id="a9017-125">-IncludeAddress</span></span>
<span data-ttu-id="a9017-126">Faturalandırma hesabının adresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-126">Include the address of the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9017-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="a9017-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="a9017-128">Faturalandırma hesabı altına faturalandırma profilini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-128">Include the billing profiles under the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9017-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="a9017-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="a9017-130">Faturalama hesabı ve fatura bölümlerinin altına faturalama profillerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9017-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9017-131">-Name</span></span>
<span data-ttu-id="a9017-132">Belirli bir faturalandırma hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a9017-132">Name of a specific billing account.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9017-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="a9017-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="a9017-134">Faturalandırma hesabı altında, abonelik oluşturmak için giriş olarak kullanılabilecek faturalandırma varlıklarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="a9017-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9017-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9017-135">CommonParameters</span></span>
<span data-ttu-id="a9017-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9017-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9017-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9017-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9017-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9017-138">INPUTS</span></span>

### <span data-ttu-id="a9017-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9017-139">None</span></span>

## <span data-ttu-id="a9017-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9017-140">OUTPUTS</span></span>

### <span data-ttu-id="a9017-141">Microsoft. Azure. Commands. faturalandırma. modeller. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="a9017-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="a9017-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9017-142">NOTES</span></span>

## <span data-ttu-id="a9017-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9017-143">RELATED LINKS</span></span>
