---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 22cc09a405d124ef4bf44342077b53dc64f974b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759105"
---
# <span data-ttu-id="2d253-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2d253-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="2d253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d253-102">SYNOPSIS</span></span>
<span data-ttu-id="2d253-103">Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d253-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="2d253-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d253-104">SYNTAX</span></span>

### <span data-ttu-id="2d253-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="2d253-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d253-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="2d253-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d253-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d253-107">DESCRIPTION</span></span>
<span data-ttu-id="2d253-108">Kümeden hizmet doku ayarlarını kaldırmak için **Remove-AzServiceFabricSetting** 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="2d253-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="2d253-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d253-109">EXAMPLES</span></span>

### <span data-ttu-id="2d253-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d253-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="2d253-111">Bu komut ' eseslerer'</span><span class="sxs-lookup"><span data-stu-id="2d253-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="2d253-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d253-112">PARAMETERS</span></span>

### <span data-ttu-id="2d253-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d253-113">-DefaultProfile</span></span>
<span data-ttu-id="2d253-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d253-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d253-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d253-115">-Name</span></span>
<span data-ttu-id="2d253-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2d253-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2d253-117">-Parametre</span><span class="sxs-lookup"><span data-stu-id="2d253-117">-Parameter</span></span>
<span data-ttu-id="2d253-118">Parametresi.</span><span class="sxs-lookup"><span data-stu-id="2d253-118">Parameter.</span></span>

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

### <span data-ttu-id="2d253-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d253-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d253-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d253-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2d253-121">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="2d253-121">-Section</span></span>
<span data-ttu-id="2d253-122">Bölümde.</span><span class="sxs-lookup"><span data-stu-id="2d253-122">Section.</span></span>

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

### <span data-ttu-id="2d253-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="2d253-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="2d253-124">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="2d253-124">Client authentication type.</span></span>

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

### <span data-ttu-id="2d253-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d253-125">-Confirm</span></span>
<span data-ttu-id="2d253-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d253-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d253-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d253-127">-WhatIf</span></span>
<span data-ttu-id="2d253-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d253-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d253-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d253-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d253-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d253-130">CommonParameters</span></span>
<span data-ttu-id="2d253-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d253-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d253-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d253-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d253-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d253-133">INPUTS</span></span>

### <span data-ttu-id="2d253-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2d253-134">System.String</span></span>

### <span data-ttu-id="2d253-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="2d253-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="2d253-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d253-136">OUTPUTS</span></span>

### <span data-ttu-id="2d253-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2d253-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2d253-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d253-138">NOTES</span></span>

## <span data-ttu-id="2d253-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d253-139">RELATED LINKS</span></span>
