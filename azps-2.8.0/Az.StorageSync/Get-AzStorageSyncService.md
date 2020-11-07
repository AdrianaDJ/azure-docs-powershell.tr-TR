---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: 9eca6930caccd2796362e32f1617ee98bcda0885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934300"
---
# <span data-ttu-id="af6b0-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="af6b0-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="af6b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af6b0-102">SYNOPSIS</span></span>
<span data-ttu-id="af6b0-103">Bu komut, belirli bir abonelik/kaynak grubu kapsamındaki tüm depolama eşitleme hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af6b0-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="af6b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af6b0-104">SYNTAX</span></span>

### <span data-ttu-id="af6b0-105">ParentStringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af6b0-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af6b0-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="af6b0-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af6b0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af6b0-107">DESCRIPTION</span></span>
<span data-ttu-id="af6b0-108">Bu komut, belirli bir abonelik/kaynak grubu kapsamındaki tüm depolama eşitleme hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="af6b0-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="af6b0-109">Tüm depolama eşitleme hizmetlerinin özniteliklerini de listelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="af6b0-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="af6b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af6b0-110">EXAMPLES</span></span>

### <span data-ttu-id="af6b0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af6b0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="af6b0-112">Bu komut, belirli bir kaynak grubundaki tüm depolama eşitleme hizmeti kaynaklarını listeler.</span><span class="sxs-lookup"><span data-stu-id="af6b0-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="af6b0-113">Tüm depolama eşitleme hizmetlerinin özniteliklerini de listelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="af6b0-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="af6b0-114">Belirli bir tane döndürmek için-StorageSyncServiceName öğesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="af6b0-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="af6b0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af6b0-115">PARAMETERS</span></span>

### <span data-ttu-id="af6b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6b0-116">-DefaultProfile</span></span>
<span data-ttu-id="af6b0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af6b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af6b0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="af6b0-118">-Name</span></span>
<span data-ttu-id="af6b0-119">Depolama eşitleme hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="af6b0-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af6b0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af6b0-120">-ResourceGroupName</span></span>
<span data-ttu-id="af6b0-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="af6b0-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af6b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6b0-122">CommonParameters</span></span>
<span data-ttu-id="af6b0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af6b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6b0-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af6b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6b0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af6b0-125">INPUTS</span></span>

### <span data-ttu-id="af6b0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="af6b0-126">System.String</span></span>

## <span data-ttu-id="af6b0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af6b0-127">OUTPUTS</span></span>

### <span data-ttu-id="af6b0-128">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="af6b0-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="af6b0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af6b0-129">NOTES</span></span>

## <span data-ttu-id="af6b0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af6b0-130">RELATED LINKS</span></span>
