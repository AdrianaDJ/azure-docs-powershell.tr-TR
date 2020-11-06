---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571030"
---
# <span data-ttu-id="a8273-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a8273-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="a8273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8273-102">SYNOPSIS</span></span>
<span data-ttu-id="a8273-103">Azure kimlik doğrulama bilgilerini dosyadan yükler.</span><span class="sxs-lookup"><span data-stu-id="a8273-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="a8273-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8273-104">SYNTAX</span></span>

### <span data-ttu-id="a8273-105">Inmemoryprofile</span><span class="sxs-lookup"><span data-stu-id="a8273-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a8273-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="a8273-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a8273-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8273-107">DESCRIPTION</span></span>
<span data-ttu-id="a8273-108">Import-AzureRmContext cmdlet, Azure ortamı ve bağlamını ayarlamak için bir dosyadan kimlik doğrulama bilgilerini yükler.</span><span class="sxs-lookup"><span data-stu-id="a8273-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="a8273-109">Geçerli oturumda çalıştırdığınız cmdlet 'ler, Azure Resource Manager 'daki isteklerin kimlik doğrulaması için bu bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="a8273-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="a8273-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8273-110">EXAMPLES</span></span>

### <span data-ttu-id="a8273-111">Örnek 1: AzureRmProfile bir bağlam Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="a8273-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a8273-112">Bu örnek, cmdlet 'e geçirilen PSAzureProfile 'daki bir bağlamı içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="a8273-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="a8273-113">Örnek 2: JSON dosyasındaki bağlamı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="a8273-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a8273-114">Bu örnek, cmdlet 'e geçirilen JSON dosyasından bir bağlam seçer.</span><span class="sxs-lookup"><span data-stu-id="a8273-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="a8273-115">Bu JSON dosyası Import-AzureRmContext 'ten oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="a8273-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="a8273-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8273-116">PARAMETERS</span></span>

### <span data-ttu-id="a8273-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="a8273-117">-AzureContext</span></span>
<span data-ttu-id="a8273-118">Bu cmdlet 'in okuduğu Azure bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8273-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="a8273-119">Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.</span><span class="sxs-lookup"><span data-stu-id="a8273-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8273-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="a8273-120">-Path</span></span>
<span data-ttu-id="a8273-121">Save-AzureRMContext kullanılarak kaydedilen bağlam bilgilerinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8273-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8273-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8273-122">-Confirm</span></span>
<span data-ttu-id="a8273-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8273-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8273-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8273-124">-WhatIf</span></span>
<span data-ttu-id="a8273-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8273-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8273-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8273-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a8273-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8273-127">INPUTS</span></span>

### <span data-ttu-id="a8273-128">Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="a8273-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="a8273-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a8273-129">System.String</span></span>

## <span data-ttu-id="a8273-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8273-130">OUTPUTS</span></span>

### <span data-ttu-id="a8273-131">Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a8273-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="a8273-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8273-132">NOTES</span></span>

## <span data-ttu-id="a8273-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8273-133">RELATED LINKS</span></span>

