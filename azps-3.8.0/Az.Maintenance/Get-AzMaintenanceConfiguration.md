---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104224"
---
# <span data-ttu-id="dafb2-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dafb2-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="dafb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dafb2-102">SYNOPSIS</span></span>
<span data-ttu-id="dafb2-103">Bakım yapılandırma kaydını alma</span><span class="sxs-lookup"><span data-stu-id="dafb2-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="dafb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dafb2-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dafb2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dafb2-105">DESCRIPTION</span></span>
<span data-ttu-id="dafb2-106">Bakım yapılandırma kaydını alma</span><span class="sxs-lookup"><span data-stu-id="dafb2-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="dafb2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dafb2-107">EXAMPLES</span></span>

### <span data-ttu-id="dafb2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dafb2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="dafb2-109">Bakım yapılandırma kaydını alma</span><span class="sxs-lookup"><span data-stu-id="dafb2-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="dafb2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dafb2-110">PARAMETERS</span></span>

### <span data-ttu-id="dafb2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafb2-111">-DefaultProfile</span></span>
<span data-ttu-id="dafb2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dafb2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dafb2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="dafb2-113">-Name</span></span>
<span data-ttu-id="dafb2-114">Bakım yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="dafb2-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dafb2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dafb2-115">-ResourceGroupName</span></span>
<span data-ttu-id="dafb2-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dafb2-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dafb2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafb2-117">CommonParameters</span></span>
<span data-ttu-id="dafb2-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dafb2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafb2-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dafb2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafb2-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dafb2-120">INPUTS</span></span>

### <span data-ttu-id="dafb2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="dafb2-121">System.String</span></span>

## <span data-ttu-id="dafb2-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dafb2-122">OUTPUTS</span></span>

### <span data-ttu-id="dafb2-123">Microsoft. Azure. Commands. Maintenance. modeller. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dafb2-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="dafb2-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dafb2-124">NOTES</span></span>

## <span data-ttu-id="dafb2-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dafb2-125">RELATED LINKS</span></span>
