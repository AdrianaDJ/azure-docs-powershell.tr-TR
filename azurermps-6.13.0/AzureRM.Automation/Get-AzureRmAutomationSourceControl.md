---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 3e7affd09e8c24c1d3c1759e78ea09a0c849ff32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592808"
---
# <span data-ttu-id="700d8-101">Get-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="700d8-101">Get-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="700d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="700d8-102">SYNOPSIS</span></span>
<span data-ttu-id="700d8-103">Azure Otomasyonu kaynak denetimlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="700d8-103">Gets a list of Azure Automation source controls.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="700d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="700d8-104">SYNTAX</span></span>

### <span data-ttu-id="700d8-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="700d8-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700d8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="700d8-106">ByName</span></span>
```
Get-AzureRmAutomationSourceControl -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="700d8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="700d8-107">DESCRIPTION</span></span>
<span data-ttu-id="700d8-108">Get-AzureRmAutomationSourceControl cmdlet 'i Otomasyon kaynak denetimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="700d8-108">The Get-AzureRmAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="700d8-109">Belirli bir kaynak denetimi almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="700d8-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="700d8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="700d8-110">EXAMPLES</span></span>

### <span data-ttu-id="700d8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="700d8-111">Example 1</span></span>
<span data-ttu-id="700d8-112">Bu komut, devAccount adlı hesapta VSTSNative adlı bir Otomasyon kaynak denetimi alır.</span><span class="sxs-lookup"><span data-stu-id="700d8-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="700d8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="700d8-113">PARAMETERS</span></span>

### <span data-ttu-id="700d8-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="700d8-114">-AutomationAccountName</span></span>
<span data-ttu-id="700d8-115">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="700d8-115">The automation account name.</span></span>

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

### <span data-ttu-id="700d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="700d8-116">-DefaultProfile</span></span>
<span data-ttu-id="700d8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="700d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="700d8-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="700d8-118">-Name</span></span>
<span data-ttu-id="700d8-119">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="700d8-119">The source control name.</span></span>

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

### <span data-ttu-id="700d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="700d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="700d8-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="700d8-121">The resource group name.</span></span>

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

### <span data-ttu-id="700d8-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="700d8-122">-SourceType</span></span>
<span data-ttu-id="700d8-123">Kaynak Denetim türü.</span><span class="sxs-lookup"><span data-stu-id="700d8-123">The source control type.</span></span>

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

### <span data-ttu-id="700d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="700d8-124">CommonParameters</span></span>
<span data-ttu-id="700d8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="700d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="700d8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="700d8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="700d8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="700d8-127">INPUTS</span></span>

### <span data-ttu-id="700d8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="700d8-128">System.String</span></span>

## <span data-ttu-id="700d8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="700d8-129">OUTPUTS</span></span>

### <span data-ttu-id="700d8-130">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="700d8-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="700d8-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="700d8-131">NOTES</span></span>

## <span data-ttu-id="700d8-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="700d8-132">RELATED LINKS</span></span>
