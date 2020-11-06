---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cbbbd23a42f2922273811a7925cbae6f6fd867f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589174"
---
# <span data-ttu-id="b8c69-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b8c69-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="b8c69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c69-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c69-103">Depolama Insight.</span><span class="sxs-lookup"><span data-stu-id="b8c69-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8c69-104">SYNTAX</span></span>

### <span data-ttu-id="b8c69-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8c69-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c69-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="b8c69-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c69-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8c69-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c69-108">**Remove-Azurermoperationalınsightsstorageınsight** cmdlet 'i çalışma alanından bir depolama anlaytöğesini siler.</span><span class="sxs-lookup"><span data-stu-id="b8c69-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="b8c69-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8c69-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c69-110">Örnek 1: ada göre bir depolama kavramı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8c69-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="b8c69-111">Bu komut Mystorageınsight adındaki depolama anlayış adını belirtilen kaynak grubundaki MyWorkspace adlı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b8c69-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="b8c69-112">Komut Force parametresini belirtmezse, böylece depolama *Anlaytanızı* kaldırmadan önce onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="b8c69-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="b8c69-113">Örnek 2: bir depolama Anlaytöğesini onaysız kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8c69-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="b8c69-114">İlk komut MyWorkspace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve $Workspace değişkeninde depolar. İkinci komut, sizden onay istemeden, Mystorage$Workspace Insight adındaki bir depolama anlaytisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b8c69-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="b8c69-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8c69-115">PARAMETERS</span></span>

### <span data-ttu-id="b8c69-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b8c69-116">-Force</span></span>
<span data-ttu-id="b8c69-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b8c69-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8c69-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8c69-118">-Name</span></span>
<span data-ttu-id="b8c69-119">Depolama anlayış adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8c69-119">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c69-120">-ResourceGroupName</span></span>
<span data-ttu-id="b8c69-121">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8c69-121">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c69-122">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="b8c69-122">-Workspace</span></span>
<span data-ttu-id="b8c69-123">Depolama kavramı içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8c69-123">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c69-124">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b8c69-124">-WorkspaceName</span></span>
<span data-ttu-id="b8c69-125">Depolama kavramı içeren çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8c69-125">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c69-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8c69-126">-Confirm</span></span>
<span data-ttu-id="b8c69-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8c69-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c69-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c69-128">-WhatIf</span></span>
<span data-ttu-id="b8c69-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8c69-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c69-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8c69-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c69-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c69-131">-DefaultProfile</span></span>
<span data-ttu-id="b8c69-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8c69-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c69-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c69-133">CommonParameters</span></span>
<span data-ttu-id="b8c69-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8c69-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c69-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c69-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c69-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8c69-136">INPUTS</span></span>

### <span data-ttu-id="b8c69-137">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8c69-137">PSWorkspace</span></span>
<span data-ttu-id="b8c69-138">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b8c69-138">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="b8c69-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8c69-139">OUTPUTS</span></span>

## <span data-ttu-id="b8c69-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8c69-140">NOTES</span></span>

## <span data-ttu-id="b8c69-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8c69-141">RELATED LINKS</span></span>

[<span data-ttu-id="b8c69-142">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b8c69-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="b8c69-143">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="b8c69-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


