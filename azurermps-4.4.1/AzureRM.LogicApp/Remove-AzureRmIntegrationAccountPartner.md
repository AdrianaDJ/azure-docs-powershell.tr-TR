---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: f10173dce7b64ccc656e2c852c6eb20230d1a7bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593098"
---
# <span data-ttu-id="d5f2f-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d5f2f-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="d5f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f2f-103">Tümleştirme hesabı ortağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5f2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5f2f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5f2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5f2f-105">DESCRIPTION</span></span>
<span data-ttu-id="d5f2f-106">**Remove-AzureRmIntegrationAccountPartner** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı ortağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="d5f2f-107">Tümleştirme hesap adını, kaynak grubu adını ve ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="d5f2f-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d5f2f-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d5f2f-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d5f2f-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d5f2f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5f2f-112">EXAMPLES</span></span>

### <span data-ttu-id="d5f2f-113">Örnek 1: Tümleştirme hesabı ortağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d5f2f-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="d5f2f-114">Bu komut, IntegrationAccountPartner1 adlı tümleştirme hesabı ortağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="d5f2f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5f2f-115">PARAMETERS</span></span>

### <span data-ttu-id="d5f2f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d5f2f-116">-Force</span></span>
<span data-ttu-id="d5f2f-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5f2f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5f2f-118">-Name</span></span>
<span data-ttu-id="d5f2f-119">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d5f2f-120">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="d5f2f-120">-PartnerName</span></span>
<span data-ttu-id="d5f2f-121">Tümleştirme hesap ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-121">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="d5f2f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f2f-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5f2f-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d5f2f-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5f2f-124">-Confirm</span></span>
<span data-ttu-id="d5f2f-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5f2f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5f2f-126">-WhatIf</span></span>
<span data-ttu-id="d5f2f-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5f2f-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5f2f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f2f-129">-DefaultProfile</span></span>
<span data-ttu-id="d5f2f-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5f2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f2f-131">CommonParameters</span></span>
<span data-ttu-id="d5f2f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5f2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f2f-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f2f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f2f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5f2f-134">INPUTS</span></span>

## <span data-ttu-id="d5f2f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5f2f-135">OUTPUTS</span></span>

## <span data-ttu-id="d5f2f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5f2f-136">NOTES</span></span>

## <span data-ttu-id="d5f2f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5f2f-137">RELATED LINKS</span></span>

[<span data-ttu-id="d5f2f-138">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d5f2f-138">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="d5f2f-139">Yeni-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d5f2f-139">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="d5f2f-140">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d5f2f-140">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


