---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 76f82e81ca9593865fea642d44bf1bde58f60eb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753253"
---
# <span data-ttu-id="9851d-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9851d-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="9851d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9851d-102">SYNOPSIS</span></span>
<span data-ttu-id="9851d-103">Otomasyon bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9851d-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="9851d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9851d-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9851d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9851d-105">DESCRIPTION</span></span>
<span data-ttu-id="9851d-106">**Remove-AzAutomationConnection** cmdlet 'ı Azure Otomasyonu 'ndan bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9851d-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="9851d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9851d-107">EXAMPLES</span></span>

### <span data-ttu-id="9851d-108">Örnek 1: bağlantı kaldırma</span><span class="sxs-lookup"><span data-stu-id="9851d-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9851d-109">Bu komut, Contoso17 adlı Otomasyon hesabındaki ContosoConnection adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9851d-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9851d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9851d-110">PARAMETERS</span></span>

### <span data-ttu-id="9851d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9851d-111">-AutomationAccountName</span></span>
<span data-ttu-id="9851d-112">Bu cmdlet 'in bağlantıyı kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9851d-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="9851d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9851d-113">-DefaultProfile</span></span>
<span data-ttu-id="9851d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9851d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9851d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9851d-115">-Force</span></span>
<span data-ttu-id="9851d-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="9851d-116">ps_force</span></span>

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

### <span data-ttu-id="9851d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9851d-117">-Name</span></span>
<span data-ttu-id="9851d-118">Bu cmdlet 'in kaldırdığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9851d-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9851d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9851d-119">-ResourceGroupName</span></span>
<span data-ttu-id="9851d-120">Bu cmdlet 'in bağlantıyı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9851d-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="9851d-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="9851d-121">-Confirm</span></span>
<span data-ttu-id="9851d-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9851d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9851d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9851d-123">-WhatIf</span></span>
<span data-ttu-id="9851d-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9851d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9851d-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9851d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9851d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9851d-126">CommonParameters</span></span>
<span data-ttu-id="9851d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9851d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9851d-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9851d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9851d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9851d-129">INPUTS</span></span>

### <span data-ttu-id="9851d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9851d-130">System.String</span></span>

## <span data-ttu-id="9851d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9851d-131">OUTPUTS</span></span>

### <span data-ttu-id="9851d-132">System. void</span><span class="sxs-lookup"><span data-stu-id="9851d-132">System.Void</span></span>

## <span data-ttu-id="9851d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9851d-133">NOTES</span></span>

## <span data-ttu-id="9851d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9851d-134">RELATED LINKS</span></span>

[<span data-ttu-id="9851d-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9851d-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="9851d-136">Yeni-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9851d-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


