---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594498"
---
# <span data-ttu-id="f6f2b-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f6f2b-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="f6f2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f2b-103">Otomasyon bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6f2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6f2b-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6f2b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f2b-106">**Remove-AzureRmAutomationConnection** cmdlet 'ı Azure Otomasyonu 'ndan bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="f6f2b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f2b-108">Örnek 1: bağlantı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f6f2b-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f6f2b-109">Bu komut, Contoso17 adlı Otomasyon hesabındaki ContosoConnection adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f6f2b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6f2b-110">PARAMETERS</span></span>

### <span data-ttu-id="f6f2b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f6f2b-111">-AutomationAccountName</span></span>
<span data-ttu-id="f6f2b-112">Bu cmdlet 'in bağlantıyı kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f2b-113">-DefaultProfile</span></span>
<span data-ttu-id="f6f2b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f6f2b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f6f2b-115">-Force</span></span>
<span data-ttu-id="f6f2b-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="f6f2b-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6f2b-117">-Name</span></span>
<span data-ttu-id="f6f2b-118">Bu cmdlet 'in kaldırdığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-118">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f2b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6f2b-120">Bu cmdlet 'in bağlantıyı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6f2b-121">-Confirm</span></span>
<span data-ttu-id="f6f2b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f2b-123">-WhatIf</span></span>
<span data-ttu-id="f6f2b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6f2b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6f2b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f2b-126">CommonParameters</span></span>
<span data-ttu-id="f6f2b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f2b-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f2b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f2b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6f2b-129">INPUTS</span></span>

### <span data-ttu-id="f6f2b-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f6f2b-130">None</span></span>
<span data-ttu-id="f6f2b-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6f2b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6f2b-132">OUTPUTS</span></span>

## <span data-ttu-id="f6f2b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6f2b-133">NOTES</span></span>

## <span data-ttu-id="f6f2b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6f2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="f6f2b-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f6f2b-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="f6f2b-136">Yeni-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f6f2b-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


