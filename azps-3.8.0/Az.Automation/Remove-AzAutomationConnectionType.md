---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104937"
---
# <span data-ttu-id="c186c-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="c186c-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="c186c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c186c-102">SYNOPSIS</span></span>
<span data-ttu-id="c186c-103">Otomasyon bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c186c-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="c186c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c186c-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c186c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c186c-105">DESCRIPTION</span></span>
<span data-ttu-id="c186c-106">**Remove-AzAutomationConnectionType** cmdlet 'ı Azure Otomasyonu 'ndan bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c186c-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="c186c-107">Sildiğiniz bağlantı türüyle ilişkili tüm bağlantılar kullanılamaz duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="c186c-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="c186c-108">Aşağıdaki ölçütlere uyan yeni bir bağlantı türü oluşturmadıkça bunları kaldırın:</span><span class="sxs-lookup"><span data-stu-id="c186c-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="c186c-109">Türün adı, özgün bağlantı türüyle aynı.</span><span class="sxs-lookup"><span data-stu-id="c186c-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="c186c-110">Tür, özgün bağlantı türüyle aynı alan tanımlarına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="c186c-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="c186c-111">Ek alanlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="c186c-111">It can have additional fields.</span></span>

## <span data-ttu-id="c186c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c186c-112">EXAMPLES</span></span>

### <span data-ttu-id="c186c-113">Örnek 1: bağlantı türünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="c186c-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c186c-114">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoConnectionType adlı bir bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c186c-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c186c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c186c-115">PARAMETERS</span></span>

### <span data-ttu-id="c186c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c186c-116">-AutomationAccountName</span></span>
<span data-ttu-id="c186c-117">Bu cmdlet 'in bağlantı türünü kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c186c-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c186c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c186c-118">-DefaultProfile</span></span>
<span data-ttu-id="c186c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c186c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c186c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c186c-120">-Force</span></span>
<span data-ttu-id="c186c-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="c186c-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c186c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c186c-122">-Name</span></span>
<span data-ttu-id="c186c-123">Bu cmdlet 'in kaldırıldığı Otomasyon bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c186c-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c186c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c186c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c186c-125">Bu cmdlet 'in Otomasyon bağlantı türünü kaldıran kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c186c-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c186c-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c186c-126">-Confirm</span></span>
<span data-ttu-id="c186c-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c186c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c186c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c186c-128">-WhatIf</span></span>
<span data-ttu-id="c186c-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c186c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c186c-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c186c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c186c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c186c-131">CommonParameters</span></span>
<span data-ttu-id="c186c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c186c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c186c-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c186c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c186c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c186c-134">INPUTS</span></span>

### <span data-ttu-id="c186c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c186c-135">System.String</span></span>

## <span data-ttu-id="c186c-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c186c-136">OUTPUTS</span></span>

### <span data-ttu-id="c186c-137">System. void</span><span class="sxs-lookup"><span data-stu-id="c186c-137">System.Void</span></span>

## <span data-ttu-id="c186c-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c186c-138">NOTES</span></span>

## <span data-ttu-id="c186c-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c186c-139">RELATED LINKS</span></span>

[<span data-ttu-id="c186c-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c186c-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


