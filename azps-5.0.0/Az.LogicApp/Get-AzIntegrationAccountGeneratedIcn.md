---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278655"
---
# <span data-ttu-id="3a455-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="3a455-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="3a455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a455-102">SYNOPSIS</span></span>
<span data-ttu-id="3a455-103">Bu cmdlet, anlaşma başına oluşturulan değişim denetim numarasının geçerli değerini alır.</span><span class="sxs-lookup"><span data-stu-id="3a455-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="3a455-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a455-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a455-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a455-105">DESCRIPTION</span></span>
<span data-ttu-id="3a455-106">Bu cmdlet, set-Azıntegrationaccountgeneratedicn ile artan bir değeri geri yazmak için, olağanüstü durum kurtarma senaryolarında kullanılacak</span><span class="sxs-lookup"><span data-stu-id="3a455-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="3a455-107">Etkin bölgede olağanüstü durum oluştuğu için, pasif bölgeye çoğaltılmamış olan sayıların yinelenen takas denetim numaralarını önlemek için, değişim denetim numarası artırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="3a455-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="3a455-108">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="3a455-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="3a455-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a455-109">EXAMPLES</span></span>

### <span data-ttu-id="3a455-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a455-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="3a455-111">Bu komut, anlaşma hesabını, anlaşma adına göre x12 Interchange Control numarasıyla üretilen tümleştirme hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="3a455-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="3a455-112">Sözleşmenin belirtilen "x12" türünde olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="3a455-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="3a455-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3a455-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="3a455-114">Bu komut, tümleştirme hesabını, anlaşma adına göre oluşturulmuş Edıbulınterchange denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="3a455-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="3a455-115">Sözleşmenin belirtilen "Ediolgu" türünde olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="3a455-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="3a455-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3a455-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="3a455-117">Bu komut, tüm oluşturulmuş x12 değişim denetim numaralarını tümleştirme hesap adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="3a455-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="3a455-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a455-118">PARAMETERS</span></span>

### <span data-ttu-id="3a455-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="3a455-119">-AgreementName</span></span>
<span data-ttu-id="3a455-120">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="3a455-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="3a455-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="3a455-121">-AgreementType</span></span>
<span data-ttu-id="3a455-122">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="3a455-122">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a455-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a455-123">-DefaultProfile</span></span>
<span data-ttu-id="3a455-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3a455-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a455-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a455-125">-Name</span></span>
<span data-ttu-id="3a455-126">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="3a455-126">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a455-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a455-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a455-128">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3a455-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="3a455-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a455-129">CommonParameters</span></span>
<span data-ttu-id="3a455-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a455-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a455-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a455-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a455-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a455-132">INPUTS</span></span>

### <span data-ttu-id="3a455-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3a455-133">System.String</span></span>

## <span data-ttu-id="3a455-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a455-134">OUTPUTS</span></span>

### <span data-ttu-id="3a455-135">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="3a455-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="3a455-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a455-136">NOTES</span></span>

## <span data-ttu-id="3a455-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a455-137">RELATED LINKS</span></span>

[<span data-ttu-id="3a455-138">Set-Azıntegrationaccountgeneratedicn</span><span class="sxs-lookup"><span data-stu-id="3a455-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

