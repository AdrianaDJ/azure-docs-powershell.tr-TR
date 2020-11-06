---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 63241b764576e06166e293f17717b26c4dcbe3d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592616"
---
# <span data-ttu-id="168c4-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="168c4-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="168c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="168c4-102">SYNOPSIS</span></span>
<span data-ttu-id="168c4-103">Tümleştirme hesabı anlaşmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="168c4-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="168c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="168c4-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="168c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="168c4-105">DESCRIPTION</span></span>
<span data-ttu-id="168c4-106">**Remove-AzureRmIntegrationAccountAgreement** cmdlet 'ı bir Azure kaynak grubundan tümleştirme hesabı anlaşmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="168c4-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="168c4-107">Tümleştirme hesap adını, kaynak grubu adını ve anlaşma adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="168c4-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="168c4-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="168c4-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="168c4-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="168c4-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="168c4-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="168c4-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="168c4-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="168c4-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="168c4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="168c4-112">EXAMPLES</span></span>

### <span data-ttu-id="168c4-113">Örnek 1: bir tümleştirme hesabı sözleşmesini ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="168c4-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="168c4-114">Bu komut, IntegrationAccountAgreement06 adlı tümleştirme hesabı sözleşmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="168c4-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="168c4-115">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="168c4-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="168c4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="168c4-116">PARAMETERS</span></span>

### <span data-ttu-id="168c4-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="168c4-117">-AgreementName</span></span>
<span data-ttu-id="168c4-118">Tümleştirme hesap anlaşmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="168c4-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="168c4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="168c4-119">-Force</span></span>
<span data-ttu-id="168c4-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="168c4-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="168c4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="168c4-121">-Name</span></span>
<span data-ttu-id="168c4-122">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="168c4-122">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="168c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="168c4-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="168c4-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="168c4-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="168c4-125">-Confirm</span></span>
<span data-ttu-id="168c4-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="168c4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="168c4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="168c4-127">-WhatIf</span></span>
<span data-ttu-id="168c4-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="168c4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="168c4-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="168c4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="168c4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168c4-130">-DefaultProfile</span></span>
<span data-ttu-id="168c4-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="168c4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="168c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168c4-132">CommonParameters</span></span>
<span data-ttu-id="168c4-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="168c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168c4-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168c4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168c4-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="168c4-135">INPUTS</span></span>

## <span data-ttu-id="168c4-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="168c4-136">OUTPUTS</span></span>

## <span data-ttu-id="168c4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="168c4-137">NOTES</span></span>

## <span data-ttu-id="168c4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="168c4-138">RELATED LINKS</span></span>

[<span data-ttu-id="168c4-139">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="168c4-139">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="168c4-140">Yeni-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="168c4-140">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="168c4-141">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="168c4-141">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


