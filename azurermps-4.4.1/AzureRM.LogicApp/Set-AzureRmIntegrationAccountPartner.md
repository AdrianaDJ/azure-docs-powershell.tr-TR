---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 13b82cbc7b1f83c441f1211f6ebe7aa1f8c59ea5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763705"
---
# <span data-ttu-id="30790-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="30790-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="30790-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30790-102">SYNOPSIS</span></span>
<span data-ttu-id="30790-103">Bir tümleştirme hesabı ortağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="30790-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30790-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30790-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30790-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30790-105">DESCRIPTION</span></span>
<span data-ttu-id="30790-106">**Set-AzureRmIntegrationAccountPartner** cmdlet 'i bir tümleştirme hesabı ortağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="30790-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="30790-107">Bu cmdlet, tümleştirme hesabı ortağını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="30790-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="30790-108">Tümleştirme hesap adını, kaynak grubu adını ve ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="30790-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="30790-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="30790-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="30790-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="30790-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="30790-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="30790-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="30790-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="30790-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="30790-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30790-113">EXAMPLES</span></span>

### <span data-ttu-id="30790-114">Örnek 1: Tümleştirme hesabı ortağını değiştirme</span><span class="sxs-lookup"><span data-stu-id="30790-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="30790-115">Bu komut, belirtilen kaynak grubundaki IntegrationAccountPartner22 adlı tümleştirme hesabı ortağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="30790-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="30790-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30790-116">PARAMETERS</span></span>

### <span data-ttu-id="30790-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="30790-117">-BusinessIdentities</span></span>
<span data-ttu-id="30790-118">Tümleştirme hesabı ortağının iş kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30790-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="30790-119">Karma bir tablo belirtin.</span><span class="sxs-lookup"><span data-stu-id="30790-119">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30790-120">-Force</span><span class="sxs-lookup"><span data-stu-id="30790-120">-Force</span></span>
<span data-ttu-id="30790-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="30790-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30790-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="30790-122">-Metadata</span></span>
<span data-ttu-id="30790-123">İş ortağı için bir meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="30790-123">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30790-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="30790-124">-Name</span></span>
<span data-ttu-id="30790-125">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30790-125">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30790-126">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="30790-126">-PartnerName</span></span>
<span data-ttu-id="30790-127">Tümleştirme hesap ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30790-127">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30790-128">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="30790-128">-PartnerType</span></span>
<span data-ttu-id="30790-129">Tümleştirme hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="30790-129">Specifies the type of the integration account.</span></span>
<span data-ttu-id="30790-130">Bu parametre, B2B türünü destekler.</span><span class="sxs-lookup"><span data-stu-id="30790-130">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30790-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30790-131">-ResourceGroupName</span></span>
<span data-ttu-id="30790-132">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30790-132">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30790-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="30790-133">-Confirm</span></span>
<span data-ttu-id="30790-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30790-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30790-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30790-135">-WhatIf</span></span>
<span data-ttu-id="30790-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30790-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30790-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30790-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30790-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30790-138">-DefaultProfile</span></span>
<span data-ttu-id="30790-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30790-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30790-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30790-140">CommonParameters</span></span>
<span data-ttu-id="30790-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30790-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30790-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30790-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30790-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30790-143">INPUTS</span></span>

## <span data-ttu-id="30790-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30790-144">OUTPUTS</span></span>

### <span data-ttu-id="30790-145">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="30790-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="30790-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30790-146">NOTES</span></span>

## <span data-ttu-id="30790-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30790-147">RELATED LINKS</span></span>

[<span data-ttu-id="30790-148">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="30790-148">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="30790-149">Yeni-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="30790-149">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="30790-150">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="30790-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


