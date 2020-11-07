---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: fa03a9a14c8024298656de1ed8bcf97bbf65378c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751495"
---
# <span data-ttu-id="dee1d-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="dee1d-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="dee1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dee1d-102">SYNOPSIS</span></span>
<span data-ttu-id="dee1d-103">Tümleştirme hesabı anlaşmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="dee1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dee1d-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dee1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dee1d-105">DESCRIPTION</span></span>
<span data-ttu-id="dee1d-106">**Set-Azıntegrationaccountagreement** cmdlet 'i bir tümleştirme hesabı anlaşmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="dee1d-107">Bu cmdlet, tümleştirme hesap anlaşmasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="dee1d-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="dee1d-108">Tümleştirme hesap adını, kaynak grubu adını ve anlaşma adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="dee1d-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="dee1d-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="dee1d-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="dee1d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dee1d-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="dee1d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dee1d-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="dee1d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dee1d-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="dee1d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dee1d-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dee1d-114">EXAMPLES</span></span>

### <span data-ttu-id="dee1d-115">Örnek 1: Tümleştirme hesabı sözleşmesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="dee1d-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="dee1d-116">Bu komut belirtilen Azure Kaynak grubunda bir tümleştirme hesabı anlaşmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="dee1d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dee1d-117">PARAMETERS</span></span>

### <span data-ttu-id="dee1d-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="dee1d-118">-AgreementContent</span></span>
<span data-ttu-id="dee1d-119">Anlaşma için, ilgili JavaScript nesne gösterimi (JSON) biçiminde anlaşma içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="dee1d-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="dee1d-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="dee1d-121">Sözleşmenin anlaşma içeriğinin dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="dee1d-122">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="dee1d-122">-AgreementName</span></span>
<span data-ttu-id="dee1d-123">Tümleştirme hesap anlaşmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="dee1d-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="dee1d-124">-AgreementType</span></span>
<span data-ttu-id="dee1d-125">Tümleştirme hesabı anlaşma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="dee1d-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dee1d-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dee1d-127">X12</span><span class="sxs-lookup"><span data-stu-id="dee1d-127">X12</span></span> 
- <span data-ttu-id="dee1d-128">AS2</span><span class="sxs-lookup"><span data-stu-id="dee1d-128">AS2</span></span>
- <span data-ttu-id="dee1d-129">Ediolgu</span><span class="sxs-lookup"><span data-stu-id="dee1d-129">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee1d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee1d-130">-DefaultProfile</span></span>
<span data-ttu-id="dee1d-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dee1d-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dee1d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="dee1d-132">-Force</span></span>
<span data-ttu-id="dee1d-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="dee1d-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dee1d-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="dee1d-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="dee1d-135">Konuk iş ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="dee1d-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="dee1d-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="dee1d-137">Tümleştirme hesap anlaşması Konuk kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="dee1d-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="dee1d-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="dee1d-138">-GuestPartner</span></span>
<span data-ttu-id="dee1d-139">Konuk ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="dee1d-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="dee1d-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="dee1d-141">Konak ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="dee1d-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="dee1d-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="dee1d-143">Tümleştirme hesabı anlaşma ana bilgisayar kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="dee1d-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="dee1d-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="dee1d-144">-HostPartner</span></span>
<span data-ttu-id="dee1d-145">Ana bilgisayar ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="dee1d-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dee1d-146">-Metadata</span></span>
<span data-ttu-id="dee1d-147">Anlaşma için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="dee1d-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="dee1d-148">-Name</span></span>
<span data-ttu-id="dee1d-149">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-149">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="dee1d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee1d-150">-ResourceGroupName</span></span>
<span data-ttu-id="dee1d-151">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dee1d-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="dee1d-152">-Confirm</span></span>
<span data-ttu-id="dee1d-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dee1d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dee1d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee1d-154">-WhatIf</span></span>
<span data-ttu-id="dee1d-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dee1d-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dee1d-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dee1d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dee1d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee1d-157">CommonParameters</span></span>
<span data-ttu-id="dee1d-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dee1d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee1d-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee1d-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee1d-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dee1d-160">INPUTS</span></span>

### <span data-ttu-id="dee1d-161">System. String</span><span class="sxs-lookup"><span data-stu-id="dee1d-161">System.String</span></span>

## <span data-ttu-id="dee1d-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dee1d-162">OUTPUTS</span></span>

### <span data-ttu-id="dee1d-163">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountagreement</span><span class="sxs-lookup"><span data-stu-id="dee1d-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="dee1d-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dee1d-164">NOTES</span></span>

## <span data-ttu-id="dee1d-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dee1d-165">RELATED LINKS</span></span>

[<span data-ttu-id="dee1d-166">Get-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="dee1d-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="dee1d-167">Yeni-azya dili muhasebe</span><span class="sxs-lookup"><span data-stu-id="dee1d-167">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="dee1d-168">Remove-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="dee1d-168">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


