---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: b95ab13e7ea35e1b41f449f461892e7ea324aa97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765166"
---
# <span data-ttu-id="7f88a-101">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7f88a-101">New-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="7f88a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f88a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f88a-103">Bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f88a-103">Creates an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f88a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f88a-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f88a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f88a-105">DESCRIPTION</span></span>
<span data-ttu-id="7f88a-106">**Yeni-AzureRmIntegrationAccountAgreement** cmdlet 'i bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f88a-106">The **New-AzureRmIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="7f88a-107">Bu cmdlet, tümleştirme hesap anlaşmasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f88a-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="7f88a-108">Tümleştirme hesap adını, kaynak grubu adını, anlaşma adını, türü, iş ortağı adını, iş ortağı niteleyicileri ve anlaşma içeriğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7f88a-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>

<span data-ttu-id="7f88a-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="7f88a-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="7f88a-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7f88a-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="7f88a-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7f88a-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="7f88a-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7f88a-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="7f88a-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7f88a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f88a-114">EXAMPLES</span></span>

### <span data-ttu-id="7f88a-115">Örnek 1: Tümleştirme hesap anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f88a-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="7f88a-116">Bu komut, belirtilen Azure Resource grubunda bir tümleştirme hesabı anlaşması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f88a-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="7f88a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f88a-117">PARAMETERS</span></span>

### <span data-ttu-id="7f88a-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="7f88a-118">-AgreementContent</span></span>
<span data-ttu-id="7f88a-119">Anlaşma için, ilgili JavaScript nesne gösterimi (JSON) biçiminde anlaşma içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="7f88a-120">Bu parametreyi veya *AgreementContentFilePath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7f88a-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="7f88a-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="7f88a-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="7f88a-122">Sözleşmenin anlaşma içeriğinin dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="7f88a-123">Bu parametreyi veya *AgreementContent* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7f88a-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="7f88a-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="7f88a-124">-AgreementName</span></span>
<span data-ttu-id="7f88a-125">Tümleştirme hesabı sözleşmesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="7f88a-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="7f88a-126">-AgreementType</span></span>
<span data-ttu-id="7f88a-127">Tümleştirme hesabı anlaşma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="7f88a-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7f88a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f88a-129">X12</span><span class="sxs-lookup"><span data-stu-id="7f88a-129">X12</span></span> 
- <span data-ttu-id="7f88a-130">AS2</span><span class="sxs-lookup"><span data-stu-id="7f88a-130">AS2</span></span>
- <span data-ttu-id="7f88a-131">Ediolgu</span><span class="sxs-lookup"><span data-stu-id="7f88a-131">Edifact</span></span>

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

### <span data-ttu-id="7f88a-132">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="7f88a-132">-GuestIdentityQualifier</span></span>
<span data-ttu-id="7f88a-133">Konuk iş ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-133">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="7f88a-134">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="7f88a-134">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="7f88a-135">Tümleştirme hesap anlaşması Konuk kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="7f88a-135">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="7f88a-136">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="7f88a-136">-GuestPartner</span></span>
<span data-ttu-id="7f88a-137">Konuk ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-137">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="7f88a-138">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="7f88a-138">-HostIdentityQualifier</span></span>
<span data-ttu-id="7f88a-139">Konak ortağı için bir ad iş kimliği niteleyicisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-139">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="7f88a-140">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="7f88a-140">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="7f88a-141">Tümleştirme hesabı anlaşma ana bilgisayar kimliği niteleyicisi değeri.</span><span class="sxs-lookup"><span data-stu-id="7f88a-141">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="7f88a-142">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="7f88a-142">-HostPartner</span></span>
<span data-ttu-id="7f88a-143">Ana bilgisayar ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-143">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="7f88a-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7f88a-144">-Metadata</span></span>
<span data-ttu-id="7f88a-145">Anlaşma için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-145">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="7f88a-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f88a-146">-Name</span></span>
<span data-ttu-id="7f88a-147">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-147">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="7f88a-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f88a-148">-ResourceGroupName</span></span>
<span data-ttu-id="7f88a-149">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-149">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7f88a-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f88a-150">-Confirm</span></span>
<span data-ttu-id="7f88a-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f88a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f88a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f88a-152">-WhatIf</span></span>
<span data-ttu-id="7f88a-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f88a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f88a-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f88a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f88a-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f88a-155">-DefaultProfile</span></span>
<span data-ttu-id="7f88a-156">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f88a-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f88a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f88a-157">CommonParameters</span></span>
<span data-ttu-id="7f88a-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f88a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f88a-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f88a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f88a-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f88a-160">INPUTS</span></span>

## <span data-ttu-id="7f88a-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f88a-161">OUTPUTS</span></span>

### <span data-ttu-id="7f88a-162">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountagreement</span><span class="sxs-lookup"><span data-stu-id="7f88a-162">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="7f88a-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f88a-163">NOTES</span></span>

## <span data-ttu-id="7f88a-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f88a-164">RELATED LINKS</span></span>

[<span data-ttu-id="7f88a-165">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7f88a-165">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7f88a-166">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7f88a-166">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7f88a-167">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7f88a-167">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


