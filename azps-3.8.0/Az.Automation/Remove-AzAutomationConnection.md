---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104936"
---
# <span data-ttu-id="52748-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="52748-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="52748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52748-102">SYNOPSIS</span></span>
<span data-ttu-id="52748-103">Otomasyon bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52748-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="52748-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52748-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52748-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52748-105">DESCRIPTION</span></span>
<span data-ttu-id="52748-106">**Remove-AzAutomationConnection** cmdlet 'ı Azure Otomasyonu 'ndan bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52748-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="52748-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52748-107">EXAMPLES</span></span>

### <span data-ttu-id="52748-108">Örnek 1: bağlantı kaldırma</span><span class="sxs-lookup"><span data-stu-id="52748-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="52748-109">Bu komut, Contoso17 adlı Otomasyon hesabındaki ContosoConnection adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52748-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="52748-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52748-110">PARAMETERS</span></span>

### <span data-ttu-id="52748-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="52748-111">-AutomationAccountName</span></span>
<span data-ttu-id="52748-112">Bu cmdlet 'in bağlantıyı kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52748-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="52748-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52748-113">-DefaultProfile</span></span>
<span data-ttu-id="52748-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52748-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52748-115">-Force</span><span class="sxs-lookup"><span data-stu-id="52748-115">-Force</span></span>
<span data-ttu-id="52748-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="52748-116">ps_force</span></span>

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

### <span data-ttu-id="52748-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="52748-117">-Name</span></span>
<span data-ttu-id="52748-118">Bu cmdlet 'in kaldırdığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52748-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="52748-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52748-119">-ResourceGroupName</span></span>
<span data-ttu-id="52748-120">Bu cmdlet 'in bağlantıyı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52748-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="52748-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="52748-121">-Confirm</span></span>
<span data-ttu-id="52748-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52748-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52748-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52748-123">-WhatIf</span></span>
<span data-ttu-id="52748-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52748-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52748-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52748-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52748-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52748-126">CommonParameters</span></span>
<span data-ttu-id="52748-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52748-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52748-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52748-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52748-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52748-129">INPUTS</span></span>

### <span data-ttu-id="52748-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52748-130">System.String</span></span>

## <span data-ttu-id="52748-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52748-131">OUTPUTS</span></span>

### <span data-ttu-id="52748-132">System. void</span><span class="sxs-lookup"><span data-stu-id="52748-132">System.Void</span></span>

## <span data-ttu-id="52748-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52748-133">NOTES</span></span>

## <span data-ttu-id="52748-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52748-134">RELATED LINKS</span></span>

[<span data-ttu-id="52748-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="52748-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="52748-136">Yeni-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="52748-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


