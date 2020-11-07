---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 570ab5c1c53f302f829a6abd57964fdffea1147d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763482"
---
# <span data-ttu-id="bf9d3-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bf9d3-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="bf9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9d3-103">Otomasyon bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf9d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf9d3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf9d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="bf9d3-106">**Remove-AzureRmAutomationConnection** cmdlet 'ı Azure Otomasyonu 'ndan bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="bf9d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf9d3-107">EXAMPLES</span></span>

### <span data-ttu-id="bf9d3-108">Örnek 1: bağlantı kaldırma</span><span class="sxs-lookup"><span data-stu-id="bf9d3-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bf9d3-109">Bu komut, Contoso17 adlı Otomasyon hesabındaki ContosoConnection adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bf9d3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf9d3-110">PARAMETERS</span></span>

### <span data-ttu-id="bf9d3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bf9d3-111">-AutomationAccountName</span></span>
<span data-ttu-id="bf9d3-112">Bu cmdlet 'in bağlantıyı kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="bf9d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9d3-113">-DefaultProfile</span></span>
<span data-ttu-id="bf9d3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bf9d3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf9d3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bf9d3-115">-Force</span></span>
<span data-ttu-id="bf9d3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="bf9d3-116">ps_force</span></span>

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

### <span data-ttu-id="bf9d3-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf9d3-117">-Name</span></span>
<span data-ttu-id="bf9d3-118">Bu cmdlet 'in kaldırdığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bf9d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="bf9d3-120">Bu cmdlet 'in bağlantıyı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="bf9d3-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf9d3-121">-Confirm</span></span>
<span data-ttu-id="bf9d3-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf9d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9d3-123">-WhatIf</span></span>
<span data-ttu-id="bf9d3-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9d3-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf9d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9d3-126">CommonParameters</span></span>
<span data-ttu-id="bf9d3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf9d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9d3-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf9d3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9d3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf9d3-129">INPUTS</span></span>

### <span data-ttu-id="bf9d3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf9d3-130">System.String</span></span>

## <span data-ttu-id="bf9d3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf9d3-131">OUTPUTS</span></span>

### <span data-ttu-id="bf9d3-132">System. void</span><span class="sxs-lookup"><span data-stu-id="bf9d3-132">System.Void</span></span>

## <span data-ttu-id="bf9d3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf9d3-133">NOTES</span></span>

## <span data-ttu-id="bf9d3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf9d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf9d3-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bf9d3-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="bf9d3-136">Yeni-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bf9d3-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

