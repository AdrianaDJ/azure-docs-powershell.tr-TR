---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 1b8e480a266459b21e6c357da156b4d4bc5165e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591174"
---
# <span data-ttu-id="a65e3-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a65e3-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="a65e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a65e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a65e3-103">Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a65e3-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a65e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a65e3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a65e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a65e3-105">DESCRIPTION</span></span>
<span data-ttu-id="a65e3-106">**Remove-AzureRmAutomationAccount** cmdlet 'i, bir kaynak grubundan Azure Otomasyonu hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a65e3-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="a65e3-107">Otomasyon hesapları hakkında daha fazla bilgi için New-AzureRmAutomationAccount cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a65e3-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="a65e3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a65e3-108">EXAMPLES</span></span>

### <span data-ttu-id="a65e3-109">Örnek 1: Otomasyon hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a65e3-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a65e3-110">Bu komut, kullanıcı doğrulaması istemeden ContosoAutomationAccount adlı bir Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a65e3-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="a65e3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a65e3-111">PARAMETERS</span></span>

### <span data-ttu-id="a65e3-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a65e3-112">-Force</span></span>
<span data-ttu-id="a65e3-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="a65e3-113">ps_force</span></span>

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

### <span data-ttu-id="a65e3-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a65e3-114">-Name</span></span>
<span data-ttu-id="a65e3-115">Bu cmdlet 'in kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65e3-115">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65e3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65e3-116">-ResourceGroupName</span></span>
<span data-ttu-id="a65e3-117">Bu cmdlet 'in Otomasyon hesabını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a65e3-117">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="a65e3-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="a65e3-118">-Confirm</span></span>
<span data-ttu-id="a65e3-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a65e3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a65e3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65e3-120">-WhatIf</span></span>
<span data-ttu-id="a65e3-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a65e3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a65e3-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a65e3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a65e3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65e3-123">-DefaultProfile</span></span>
<span data-ttu-id="a65e3-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a65e3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a65e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65e3-125">CommonParameters</span></span>
<span data-ttu-id="a65e3-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a65e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65e3-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a65e3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65e3-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a65e3-128">INPUTS</span></span>

## <span data-ttu-id="a65e3-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a65e3-129">OUTPUTS</span></span>

### <span data-ttu-id="a65e3-130">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a65e3-130">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="a65e3-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a65e3-131">NOTES</span></span>

## <span data-ttu-id="a65e3-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a65e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="a65e3-133">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a65e3-133">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="a65e3-134">Yeni-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a65e3-134">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="a65e3-135">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a65e3-135">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


