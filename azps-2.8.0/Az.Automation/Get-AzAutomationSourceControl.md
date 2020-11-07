---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: e960b1d68b57ef51ef51a6bd00365242e78f47a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753298"
---
# <span data-ttu-id="7d899-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="7d899-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="7d899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d899-102">SYNOPSIS</span></span>
<span data-ttu-id="7d899-103">Azure Otomasyonu kaynak denetimlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7d899-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="7d899-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d899-104">SYNTAX</span></span>

### <span data-ttu-id="7d899-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d899-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d899-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7d899-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d899-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d899-107">DESCRIPTION</span></span>
<span data-ttu-id="7d899-108">Get-AzAutomationSourceControl cmdlet 'i Otomasyon kaynak denetimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="7d899-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="7d899-109">Belirli bir kaynak denetimi almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7d899-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="7d899-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d899-110">EXAMPLES</span></span>

### <span data-ttu-id="7d899-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7d899-111">Example 1</span></span>
<span data-ttu-id="7d899-112">Bu komut, devAccount adlı hesapta VSTSNative adlı bir Otomasyon kaynak denetimi alır.</span><span class="sxs-lookup"><span data-stu-id="7d899-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="7d899-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d899-113">PARAMETERS</span></span>

### <span data-ttu-id="7d899-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7d899-114">-AutomationAccountName</span></span>
<span data-ttu-id="7d899-115">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="7d899-115">The automation account name.</span></span>

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

### <span data-ttu-id="7d899-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d899-116">-DefaultProfile</span></span>
<span data-ttu-id="7d899-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d899-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d899-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d899-118">-Name</span></span>
<span data-ttu-id="7d899-119">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="7d899-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d899-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d899-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d899-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7d899-121">The resource group name.</span></span>

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

### <span data-ttu-id="7d899-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="7d899-122">-SourceType</span></span>
<span data-ttu-id="7d899-123">Kaynak Denetim türü.</span><span class="sxs-lookup"><span data-stu-id="7d899-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d899-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d899-124">CommonParameters</span></span>
<span data-ttu-id="7d899-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d899-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d899-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d899-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d899-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d899-127">INPUTS</span></span>

### <span data-ttu-id="7d899-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7d899-128">System.String</span></span>

## <span data-ttu-id="7d899-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d899-129">OUTPUTS</span></span>

### <span data-ttu-id="7d899-130">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="7d899-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="7d899-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d899-131">NOTES</span></span>

## <span data-ttu-id="7d899-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d899-132">RELATED LINKS</span></span>