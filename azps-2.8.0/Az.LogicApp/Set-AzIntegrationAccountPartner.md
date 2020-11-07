---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: ae9b9f37a20f63a502da2904fd6d94f8a6aa281f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751485"
---
# <span data-ttu-id="8b32d-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8b32d-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="8b32d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b32d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b32d-103">Bir tümleştirme hesabı ortağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="8b32d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b32d-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b32d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b32d-105">DESCRIPTION</span></span>
<span data-ttu-id="8b32d-106">**Set-Azıntegrationaccountpartner** cmdlet 'i bir tümleştirme hesabı ortağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="8b32d-107">Bu cmdlet, tümleştirme hesabı ortağını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b32d-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="8b32d-108">Tümleştirme hesap adını, kaynak grubu adını ve ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b32d-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="8b32d-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8b32d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8b32d-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="8b32d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8b32d-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="8b32d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8b32d-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="8b32d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8b32d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b32d-113">EXAMPLES</span></span>

### <span data-ttu-id="8b32d-114">Örnek 1: Tümleştirme hesabı ortağını değiştirme</span><span class="sxs-lookup"><span data-stu-id="8b32d-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="8b32d-115">Bu komut, belirtilen kaynak grubundaki IntegrationAccountPartner22 adlı tümleştirme hesabı ortağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="8b32d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b32d-116">PARAMETERS</span></span>

### <span data-ttu-id="8b32d-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="8b32d-117">-BusinessIdentities</span></span>
<span data-ttu-id="8b32d-118">Tümleştirme hesabı ortağının iş kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="8b32d-119">Karma bir tablo belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b32d-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="8b32d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b32d-120">-DefaultProfile</span></span>
<span data-ttu-id="8b32d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8b32d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b32d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8b32d-122">-Force</span></span>
<span data-ttu-id="8b32d-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8b32d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b32d-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8b32d-124">-Metadata</span></span>
<span data-ttu-id="8b32d-125">İş ortağı için bir meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="8b32d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b32d-126">-Name</span></span>
<span data-ttu-id="8b32d-127">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="8b32d-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="8b32d-128">-PartnerName</span></span>
<span data-ttu-id="8b32d-129">Tümleştirme hesap ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="8b32d-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="8b32d-130">-PartnerType</span></span>
<span data-ttu-id="8b32d-131">Tümleştirme hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="8b32d-132">Bu parametre, B2B türünü destekler.</span><span class="sxs-lookup"><span data-stu-id="8b32d-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="8b32d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b32d-133">-ResourceGroupName</span></span>
<span data-ttu-id="8b32d-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b32d-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b32d-135">-Confirm</span></span>
<span data-ttu-id="8b32d-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b32d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b32d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b32d-137">-WhatIf</span></span>
<span data-ttu-id="8b32d-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b32d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b32d-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b32d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b32d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b32d-140">CommonParameters</span></span>
<span data-ttu-id="8b32d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b32d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b32d-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b32d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b32d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b32d-143">INPUTS</span></span>

### <span data-ttu-id="8b32d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8b32d-144">System.String</span></span>

## <span data-ttu-id="8b32d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b32d-145">OUTPUTS</span></span>

### <span data-ttu-id="8b32d-146">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="8b32d-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="8b32d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b32d-147">NOTES</span></span>

## <span data-ttu-id="8b32d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b32d-148">RELATED LINKS</span></span>

[<span data-ttu-id="8b32d-149">Get-Azıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="8b32d-149">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="8b32d-150">Yeni-az</span><span class="sxs-lookup"><span data-stu-id="8b32d-150">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="8b32d-151">Remove-Azıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="8b32d-151">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


