---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280149"
---
# <span data-ttu-id="22c39-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="22c39-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="22c39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c39-102">SYNOPSIS</span></span>
<span data-ttu-id="22c39-103">Bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22c39-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="22c39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22c39-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c39-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22c39-105">DESCRIPTION</span></span>
<span data-ttu-id="22c39-106">**New-Azıntegrationaccountagreement** cmdlet 'i bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22c39-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="22c39-107">Bu cmdlet, tümleştirme hesap anlaşmasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="22c39-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="22c39-108">Tümleştirme hesap adını, kaynak grubu adını, anlaşma adını, türü, iş ortağı adını, iş ortağı niteleyicileri ve anlaşma içeriğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="22c39-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="22c39-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="22c39-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="22c39-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="22c39-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="22c39-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="22c39-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="22c39-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="22c39-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="22c39-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="22c39-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="22c39-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22c39-114">EXAMPLES</span></span>

### <span data-ttu-id="22c39-115">Örnek 1: Tümleştirme hesap anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="22c39-115">Example 1: Create a integration account agreement</span></span>
```powershell
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

<span data-ttu-id="22c39-116">Bu komut, belirtilen Azure Resource grubunda bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22c39-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="22c39-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="22c39-117">Example 2</span></span>

<span data-ttu-id="22c39-118">Bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22c39-118">Creates an integration account agreement.</span></span> <span data-ttu-id="22c39-119">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="22c39-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="22c39-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22c39-120">PARAMETERS</span></span>

### <span data-ttu-id="22c39-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="22c39-121">-AgreementContent</span></span>
<span data-ttu-id="22c39-122">Anlaşma için, ilgili JavaScript nesne gösterimi (JSON) biçiminde anlaşma içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="22c39-123">Bu parametreyi veya *AgreementContentFilePath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="22c39-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="22c39-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="22c39-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="22c39-125">Sözleşmenin anlaşma içeriğinin dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="22c39-126">Bu parametreyi veya *AgreementContent* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="22c39-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="22c39-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="22c39-127">-AgreementName</span></span>
<span data-ttu-id="22c39-128">Tümleştirme hesabı sözleşmesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="22c39-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="22c39-129">-AgreementType</span></span>
<span data-ttu-id="22c39-130">Tümleştirme hesabı anlaşma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="22c39-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="22c39-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22c39-132">X12</span><span class="sxs-lookup"><span data-stu-id="22c39-132">X12</span></span> 
- <span data-ttu-id="22c39-133">AS2</span><span class="sxs-lookup"><span data-stu-id="22c39-133">AS2</span></span>
- <span data-ttu-id="22c39-134">Ediolgu</span><span class="sxs-lookup"><span data-stu-id="22c39-134">Edifact</span></span>

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

### <span data-ttu-id="22c39-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c39-135">-DefaultProfile</span></span>
<span data-ttu-id="22c39-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="22c39-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22c39-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="22c39-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="22c39-138">Konuk iş ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="22c39-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="22c39-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="22c39-140">Tümleştirme hesap anlaşması Konuk kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="22c39-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="22c39-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="22c39-141">-GuestPartner</span></span>
<span data-ttu-id="22c39-142">Konuk ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="22c39-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="22c39-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="22c39-144">Konak ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="22c39-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="22c39-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="22c39-146">Tümleştirme hesabı anlaşma ana bilgisayar kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="22c39-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="22c39-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="22c39-147">-HostPartner</span></span>
<span data-ttu-id="22c39-148">Ana bilgisayar ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="22c39-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="22c39-149">-Metadata</span></span>
<span data-ttu-id="22c39-150">Anlaşma için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="22c39-151">-Ad</span><span class="sxs-lookup"><span data-stu-id="22c39-151">-Name</span></span>
<span data-ttu-id="22c39-152">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="22c39-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c39-153">-ResourceGroupName</span></span>
<span data-ttu-id="22c39-154">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c39-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="22c39-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="22c39-155">-Confirm</span></span>
<span data-ttu-id="22c39-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22c39-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c39-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c39-157">-WhatIf</span></span>
<span data-ttu-id="22c39-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22c39-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c39-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22c39-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c39-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c39-160">CommonParameters</span></span>
<span data-ttu-id="22c39-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22c39-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c39-162">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c39-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c39-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22c39-163">INPUTS</span></span>

### <span data-ttu-id="22c39-164">System. String</span><span class="sxs-lookup"><span data-stu-id="22c39-164">System.String</span></span>

## <span data-ttu-id="22c39-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22c39-165">OUTPUTS</span></span>

### <span data-ttu-id="22c39-166">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountagreement</span><span class="sxs-lookup"><span data-stu-id="22c39-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="22c39-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22c39-167">NOTES</span></span>

## <span data-ttu-id="22c39-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22c39-168">RELATED LINKS</span></span>

[<span data-ttu-id="22c39-169">Get-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="22c39-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="22c39-170">Remove-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="22c39-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="22c39-171">Set-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="22c39-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


