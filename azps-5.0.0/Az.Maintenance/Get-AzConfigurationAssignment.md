---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277357"
---
# <span data-ttu-id="b8ddc-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b8ddc-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="b8ddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ddc-103">Kaynak için yapılandırma atamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b8ddc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8ddc-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8ddc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ddc-106">Kaynak için yapılandırma atamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b8ddc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8ddc-107">EXAMPLES</span></span>

### <span data-ttu-id="b8ddc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b8ddc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="b8ddc-109">Adanmış ana bilgisayar için Configurationatamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="b8ddc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8ddc-110">PARAMETERS</span></span>

### <span data-ttu-id="b8ddc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ddc-111">-DefaultProfile</span></span>
<span data-ttu-id="b8ddc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8ddc-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="b8ddc-113">-ProviderName</span></span>
<span data-ttu-id="b8ddc-114">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="b8ddc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ddc-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8ddc-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="b8ddc-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b8ddc-117">-ResourceName</span></span>
<span data-ttu-id="b8ddc-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-118">The resource name.</span></span>

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

### <span data-ttu-id="b8ddc-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="b8ddc-119">-ResourceParentName</span></span>
<span data-ttu-id="b8ddc-120">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="b8ddc-121">-ResourceParentType</span></span>
<span data-ttu-id="b8ddc-122">Üst kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b8ddc-123">-ResourceType</span></span>
<span data-ttu-id="b8ddc-124">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-124">The resource type.</span></span>

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

### <span data-ttu-id="b8ddc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ddc-125">CommonParameters</span></span>
<span data-ttu-id="b8ddc-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ddc-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ddc-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8ddc-128">INPUTS</span></span>

### <span data-ttu-id="b8ddc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b8ddc-129">System.String</span></span>

## <span data-ttu-id="b8ddc-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8ddc-130">OUTPUTS</span></span>

### <span data-ttu-id="b8ddc-131">Microsoft. Azure. Commands. Maintenance. modeller. Psconfigurationödev</span><span class="sxs-lookup"><span data-stu-id="b8ddc-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="b8ddc-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8ddc-132">NOTES</span></span>

## <span data-ttu-id="b8ddc-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8ddc-133">RELATED LINKS</span></span>
