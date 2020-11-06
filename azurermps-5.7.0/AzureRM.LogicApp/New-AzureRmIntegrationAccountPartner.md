---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 470a400721d911e09c7bed4e51eb6cef39a1dafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591666"
---
# <span data-ttu-id="e9a31-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e9a31-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="e9a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a31-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a31-103">Bir tümleştirme hesabı ortağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9a31-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9a31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9a31-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9a31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9a31-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a31-106">**Yeni-AzureRmIntegrationAccountPartner** cmdlet 'i bir tümleştirme hesabı ortağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9a31-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="e9a31-107">Bu cmdlet, tümleştirme hesabı ortağını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9a31-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="e9a31-108">Tümleştirme hesap adını, kaynak grubu adını, iş ortağı adını ve iş ortağı kimliklerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e9a31-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="e9a31-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="e9a31-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="e9a31-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e9a31-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="e9a31-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e9a31-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="e9a31-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e9a31-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="e9a31-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e9a31-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9a31-114">EXAMPLES</span></span>

### <span data-ttu-id="e9a31-115">Örnek 1: Tümleştirme hesap ortağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e9a31-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="e9a31-116">Bu komut, belirtilen kaynak grubunda IntegrationAccountPartner22 adlı tümleştirme hesabı ortağını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9a31-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="e9a31-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9a31-117">PARAMETERS</span></span>

### <span data-ttu-id="e9a31-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="e9a31-118">-BusinessIdentities</span></span>
<span data-ttu-id="e9a31-119">Tümleştirme hesabı ortağının iş kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="e9a31-120">Karma bir tablo belirtin.</span><span class="sxs-lookup"><span data-stu-id="e9a31-120">Specify a hash table.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a31-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a31-121">-DefaultProfile</span></span>
<span data-ttu-id="e9a31-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9a31-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9a31-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e9a31-123">-Metadata</span></span>
<span data-ttu-id="e9a31-124">İş ortağı için bir meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a31-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9a31-125">-Name</span></span>
<span data-ttu-id="e9a31-126">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-126">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a31-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="e9a31-127">-PartnerName</span></span>
<span data-ttu-id="e9a31-128">Tümleştirme hesabı ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-128">Specifies a name for the integration account partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a31-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="e9a31-129">-PartnerType</span></span>
<span data-ttu-id="e9a31-130">Tümleştirme hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="e9a31-131">Bu parametre, B2B türünü destekler.</span><span class="sxs-lookup"><span data-stu-id="e9a31-131">This parameter supports the type B2B.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a31-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a31-132">-ResourceGroupName</span></span>
<span data-ttu-id="e9a31-133">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-133">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a31-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9a31-134">-Confirm</span></span>
<span data-ttu-id="e9a31-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9a31-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a31-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a31-136">-WhatIf</span></span>
<span data-ttu-id="e9a31-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9a31-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a31-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9a31-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a31-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a31-139">CommonParameters</span></span>
<span data-ttu-id="e9a31-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9a31-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a31-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9a31-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a31-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9a31-142">INPUTS</span></span>

### <span data-ttu-id="e9a31-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e9a31-143">None</span></span>
<span data-ttu-id="e9a31-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e9a31-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9a31-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9a31-145">OUTPUTS</span></span>

### <span data-ttu-id="e9a31-146">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="e9a31-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="e9a31-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9a31-147">NOTES</span></span>

## <span data-ttu-id="e9a31-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9a31-148">RELATED LINKS</span></span>

[<span data-ttu-id="e9a31-149">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e9a31-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="e9a31-150">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e9a31-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="e9a31-151">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e9a31-151">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


