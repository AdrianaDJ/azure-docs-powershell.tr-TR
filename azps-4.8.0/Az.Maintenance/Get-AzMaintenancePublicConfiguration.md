---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267125"
---
# <span data-ttu-id="7e444-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e444-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="7e444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e444-102">SYNOPSIS</span></span>
<span data-ttu-id="7e444-103">Genel bakım yapılandırma kaydını alma</span><span class="sxs-lookup"><span data-stu-id="7e444-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="7e444-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e444-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e444-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e444-105">DESCRIPTION</span></span>
<span data-ttu-id="7e444-106">Genel bakım yapılandırma kaydını alma</span><span class="sxs-lookup"><span data-stu-id="7e444-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="7e444-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e444-107">EXAMPLES</span></span>

### <span data-ttu-id="7e444-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e444-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="7e444-109">Genel bakım yapılandırma kaydını alma</span><span class="sxs-lookup"><span data-stu-id="7e444-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="7e444-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e444-110">PARAMETERS</span></span>

### <span data-ttu-id="7e444-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e444-111">-DefaultProfile</span></span>
<span data-ttu-id="7e444-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e444-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e444-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e444-113">-Name</span></span>
<span data-ttu-id="7e444-114">Genel bakım yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="7e444-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e444-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e444-115">-ResourceGroupName</span></span>
<span data-ttu-id="7e444-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7e444-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e444-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e444-117">CommonParameters</span></span>
<span data-ttu-id="7e444-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e444-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e444-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e444-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e444-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e444-120">INPUTS</span></span>

### <span data-ttu-id="7e444-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7e444-121">System.String</span></span>

## <span data-ttu-id="7e444-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e444-122">OUTPUTS</span></span>

### <span data-ttu-id="7e444-123">Microsoft. Azure. Commands. Maintenance. modeller. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e444-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="7e444-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e444-124">NOTES</span></span>

## <span data-ttu-id="7e444-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e444-125">RELATED LINKS</span></span>
