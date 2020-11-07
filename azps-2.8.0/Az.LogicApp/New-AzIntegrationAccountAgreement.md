---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 10cd1993acccf45e39a1b192f44b715b06f6d1d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751533"
---
# <span data-ttu-id="7d0dc-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7d0dc-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="7d0dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d0dc-103">Bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="7d0dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d0dc-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d0dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d0dc-105">DESCRIPTION</span></span>
<span data-ttu-id="7d0dc-106">**New-Azıntegrationaccountagreement** cmdlet 'i bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="7d0dc-107">Bu cmdlet, tümleştirme hesap anlaşmasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="7d0dc-108">Tümleştirme hesap adını, kaynak grubu adını, anlaşma adını, türü, iş ortağı adını, iş ortağı niteleyicileri ve anlaşma içeriğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="7d0dc-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="7d0dc-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7d0dc-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7d0dc-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7d0dc-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7d0dc-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d0dc-114">EXAMPLES</span></span>

### <span data-ttu-id="7d0dc-115">Örnek 1: Tümleştirme hesap anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7d0dc-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="7d0dc-116">Bu komut, belirtilen Azure Resource grubunda bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="7d0dc-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d0dc-117">PARAMETERS</span></span>

### <span data-ttu-id="7d0dc-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="7d0dc-118">-AgreementContent</span></span>
<span data-ttu-id="7d0dc-119">Anlaşma için, ilgili JavaScript nesne gösterimi (JSON) biçiminde anlaşma içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="7d0dc-120">Bu parametreyi veya *AgreementContentFilePath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="7d0dc-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="7d0dc-122">Sözleşmenin anlaşma içeriğinin dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="7d0dc-123">Bu parametreyi veya *AgreementContent* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="7d0dc-124">-AgreementName</span></span>
<span data-ttu-id="7d0dc-125">Tümleştirme hesabı sözleşmesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="7d0dc-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="7d0dc-126">-AgreementType</span></span>
<span data-ttu-id="7d0dc-127">Tümleştirme hesabı anlaşma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="7d0dc-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7d0dc-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7d0dc-129">X12</span><span class="sxs-lookup"><span data-stu-id="7d0dc-129">X12</span></span> 
- <span data-ttu-id="7d0dc-130">AS2</span><span class="sxs-lookup"><span data-stu-id="7d0dc-130">AS2</span></span>
- <span data-ttu-id="7d0dc-131">Ediolgu</span><span class="sxs-lookup"><span data-stu-id="7d0dc-131">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d0dc-132">-DefaultProfile</span></span>
<span data-ttu-id="7d0dc-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7d0dc-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d0dc-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="7d0dc-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="7d0dc-135">Konuk iş ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-135">Specifies a name business identity qualifier for the guest partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="7d0dc-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="7d0dc-137">Tümleştirme hesap anlaşması Konuk kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-137">The integration account agreement guest identity qualifier value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="7d0dc-138">-GuestPartner</span></span>
<span data-ttu-id="7d0dc-139">Konuk ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-139">Specifies the name of the guest partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="7d0dc-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="7d0dc-141">Konak ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-141">Specifies a name business identity qualifier for the host partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="7d0dc-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="7d0dc-143">Tümleştirme hesabı anlaşma ana bilgisayar kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-143">The integration account agreement host identity qualifier value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="7d0dc-144">-HostPartner</span></span>
<span data-ttu-id="7d0dc-145">Ana bilgisayar ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-145">Specifies the name of the host partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0dc-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7d0dc-146">-Metadata</span></span>
<span data-ttu-id="7d0dc-147">Anlaşma için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="7d0dc-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d0dc-148">-Name</span></span>
<span data-ttu-id="7d0dc-149">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-149">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="7d0dc-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d0dc-150">-ResourceGroupName</span></span>
<span data-ttu-id="7d0dc-151">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7d0dc-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="7d0dc-152">-Confirm</span></span>
<span data-ttu-id="7d0dc-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d0dc-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d0dc-154">-WhatIf</span></span>
<span data-ttu-id="7d0dc-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d0dc-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d0dc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0dc-157">CommonParameters</span></span>
<span data-ttu-id="7d0dc-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d0dc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0dc-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d0dc-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0dc-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d0dc-160">INPUTS</span></span>

### <span data-ttu-id="7d0dc-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7d0dc-161">System.String</span></span>

## <span data-ttu-id="7d0dc-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d0dc-162">OUTPUTS</span></span>

### <span data-ttu-id="7d0dc-163">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountagreement</span><span class="sxs-lookup"><span data-stu-id="7d0dc-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="7d0dc-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d0dc-164">NOTES</span></span>

## <span data-ttu-id="7d0dc-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d0dc-165">RELATED LINKS</span></span>

[<span data-ttu-id="7d0dc-166">Get-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="7d0dc-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="7d0dc-167">Remove-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="7d0dc-167">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="7d0dc-168">Set-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="7d0dc-168">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


