---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: b2933a5c6229315ac132aade6a3cb3ef3e9a964c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764375"
---
# <span data-ttu-id="bb081-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bb081-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="bb081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb081-102">SYNOPSIS</span></span>
<span data-ttu-id="bb081-103">Bir tümleştirme hesabı anlaşmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bb081-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb081-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb081-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb081-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb081-105">DESCRIPTION</span></span>
<span data-ttu-id="bb081-106">**Get-AzureRmIntegrationAccountAgreement** cmdlet 'ı bir Azure kaynak grubundan bir tümleştirme hesabı anlaşmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bb081-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="bb081-107">Tümleştirme hesap adını, kaynak grubu adını ve anlaşma adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="bb081-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="bb081-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="bb081-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bb081-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="bb081-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bb081-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="bb081-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bb081-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="bb081-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bb081-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb081-112">EXAMPLES</span></span>

### <span data-ttu-id="bb081-113">Örnek 1: Tümleştirme hesabı anlaşması alma</span><span class="sxs-lookup"><span data-stu-id="bb081-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="bb081-114">Bu komut, IntegrationAccountAgreement06 adlı bir tümleştirme hesabı anlaşmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bb081-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="bb081-115">Örnek 2: kaynak grubu adına göre tümleştirme hesap sözleşmelerini alma</span><span class="sxs-lookup"><span data-stu-id="bb081-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="bb081-116">Bu komut, tümleştirme hesap sözleşmelerini kaynak grubu adına göre alır.</span><span class="sxs-lookup"><span data-stu-id="bb081-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="bb081-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb081-117">PARAMETERS</span></span>

### <span data-ttu-id="bb081-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="bb081-118">-AgreementName</span></span>
<span data-ttu-id="bb081-119">Tümleştirme hesap anlaşmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb081-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="bb081-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb081-120">-DefaultProfile</span></span>
<span data-ttu-id="bb081-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bb081-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb081-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb081-122">-Name</span></span>
<span data-ttu-id="bb081-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb081-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb081-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb081-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb081-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb081-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb081-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb081-126">CommonParameters</span></span>
<span data-ttu-id="bb081-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb081-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb081-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb081-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb081-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb081-129">INPUTS</span></span>

### <span data-ttu-id="bb081-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bb081-130">System.String</span></span>

## <span data-ttu-id="bb081-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb081-131">OUTPUTS</span></span>

### <span data-ttu-id="bb081-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountagreement</span><span class="sxs-lookup"><span data-stu-id="bb081-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="bb081-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb081-133">NOTES</span></span>

## <span data-ttu-id="bb081-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb081-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb081-135">Yeni-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bb081-135">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="bb081-136">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bb081-136">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="bb081-137">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bb081-137">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


