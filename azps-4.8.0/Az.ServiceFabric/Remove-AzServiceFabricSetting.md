---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108721"
---
# <span data-ttu-id="2c45f-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2c45f-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="2c45f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c45f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c45f-103">Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2c45f-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="2c45f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c45f-104">SYNTAX</span></span>

### <span data-ttu-id="2c45f-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="2c45f-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c45f-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="2c45f-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c45f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c45f-107">DESCRIPTION</span></span>
<span data-ttu-id="2c45f-108">Kümeden hizmet doku ayarlarını kaldırmak için **Remove-AzServiceFabricSetting** 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="2c45f-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="2c45f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c45f-109">EXAMPLES</span></span>

### <span data-ttu-id="2c45f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c45f-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="2c45f-111">Bu komut ' eseslerer'</span><span class="sxs-lookup"><span data-stu-id="2c45f-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="2c45f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c45f-112">PARAMETERS</span></span>

### <span data-ttu-id="2c45f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c45f-113">-DefaultProfile</span></span>
<span data-ttu-id="2c45f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c45f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c45f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c45f-115">-Name</span></span>
<span data-ttu-id="2c45f-116">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="2c45f-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c45f-117">-Parametre</span><span class="sxs-lookup"><span data-stu-id="2c45f-117">-Parameter</span></span>
<span data-ttu-id="2c45f-118">Doku ayarının parametre adı</span><span class="sxs-lookup"><span data-stu-id="2c45f-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c45f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c45f-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c45f-120">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2c45f-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2c45f-121">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="2c45f-121">-Section</span></span>
<span data-ttu-id="2c45f-122">Doku ayarının bölüm adı</span><span class="sxs-lookup"><span data-stu-id="2c45f-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c45f-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="2c45f-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="2c45f-124">Doku ayarları dizisi</span><span class="sxs-lookup"><span data-stu-id="2c45f-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c45f-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c45f-125">-Confirm</span></span>
<span data-ttu-id="2c45f-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c45f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c45f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c45f-127">-WhatIf</span></span>
<span data-ttu-id="2c45f-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c45f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c45f-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c45f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c45f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c45f-130">CommonParameters</span></span>
<span data-ttu-id="2c45f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c45f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c45f-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2c45f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c45f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c45f-133">INPUTS</span></span>

### <span data-ttu-id="2c45f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2c45f-134">System.String</span></span>

### <span data-ttu-id="2c45f-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="2c45f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="2c45f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c45f-136">OUTPUTS</span></span>

### <span data-ttu-id="2c45f-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2c45f-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2c45f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c45f-138">NOTES</span></span>

## <span data-ttu-id="2c45f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c45f-139">RELATED LINKS</span></span>
