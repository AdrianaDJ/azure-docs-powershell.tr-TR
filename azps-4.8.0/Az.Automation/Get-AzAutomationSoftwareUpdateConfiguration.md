---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268127"
---
# <span data-ttu-id="f7c7d-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7c7d-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f7c7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c7d-103">Azure Otomasyonu yazılım güncelleştirme yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="f7c7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7c7d-104">SYNTAX</span></span>

### <span data-ttu-id="f7c7d-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7c7d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7c7d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f7c7d-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7c7d-107">Byvmıd</span><span class="sxs-lookup"><span data-stu-id="f7c7d-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7c7d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7c7d-108">DESCRIPTION</span></span>
<span data-ttu-id="f7c7d-109">Get-AzAutomationSoftwareUpdateConfiguration yazılım güncelleştirmesi yapılandırmalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="f7c7d-110">Belirli bir yazılım güncelleştirmesi yapılandırması edinmek için, ad parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="f7c7d-111">Bu sanal makine için Azure Resource ID belirterek belirli Azure sanal makinesini hedefleyen yazılım güncelleştirme yapılandırmalarını da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="f7c7d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7c7d-112">EXAMPLES</span></span>

### <span data-ttu-id="f7c7d-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f7c7d-113">Example 1</span></span>
<span data-ttu-id="f7c7d-114">Azure Otomasyonu yazılım güncelleştirme yapılandırmasını ada göre edinin.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="f7c7d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7c7d-115">PARAMETERS</span></span>

### <span data-ttu-id="f7c7d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7c7d-116">-AutomationAccountName</span></span>
<span data-ttu-id="f7c7d-117">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-117">The automation account name.</span></span>

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

### <span data-ttu-id="f7c7d-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="f7c7d-118">-AzureVMResourceId</span></span>
<span data-ttu-id="f7c7d-119">Sanal makinenin Azure kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c7d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c7d-120">-DefaultProfile</span></span>
<span data-ttu-id="f7c7d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7c7d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7c7d-122">-Name</span></span>
<span data-ttu-id="f7c7d-123">Yazılım güncelleştirme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="f7c7d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c7d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7c7d-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-125">The resource group name.</span></span>

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

### <span data-ttu-id="f7c7d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c7d-126">CommonParameters</span></span>
<span data-ttu-id="f7c7d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7c7d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c7d-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c7d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c7d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7c7d-129">INPUTS</span></span>

### <span data-ttu-id="f7c7d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7c7d-130">System.String</span></span>

## <span data-ttu-id="f7c7d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7c7d-131">OUTPUTS</span></span>

### <span data-ttu-id="f7c7d-132">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7c7d-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f7c7d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7c7d-133">NOTES</span></span>

## <span data-ttu-id="f7c7d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7c7d-134">RELATED LINKS</span></span>
