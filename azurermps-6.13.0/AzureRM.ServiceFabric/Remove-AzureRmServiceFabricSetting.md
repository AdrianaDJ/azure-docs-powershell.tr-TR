---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 4643ab29be9c93f58895048317edc2b1db6115e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764115"
---
# <span data-ttu-id="78d11-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="78d11-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="78d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d11-102">SYNOPSIS</span></span>
<span data-ttu-id="78d11-103">Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="78d11-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78d11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78d11-104">SYNTAX</span></span>

### <span data-ttu-id="78d11-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="78d11-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d11-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="78d11-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d11-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="78d11-107">DESCRIPTION</span></span>
<span data-ttu-id="78d11-108">Kümeden hizmet doku ayarlarını kaldırmak için **Remove-AzureRmServiceFabricSetting** 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="78d11-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="78d11-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78d11-109">EXAMPLES</span></span>

### <span data-ttu-id="78d11-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="78d11-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="78d11-111">Bu komut ' eseslerer'</span><span class="sxs-lookup"><span data-stu-id="78d11-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="78d11-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78d11-112">PARAMETERS</span></span>

### <span data-ttu-id="78d11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d11-113">-DefaultProfile</span></span>
<span data-ttu-id="78d11-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78d11-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78d11-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="78d11-115">-Name</span></span>
<span data-ttu-id="78d11-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="78d11-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="78d11-117">-Parametre</span><span class="sxs-lookup"><span data-stu-id="78d11-117">-Parameter</span></span>
<span data-ttu-id="78d11-118">Parametresi.</span><span class="sxs-lookup"><span data-stu-id="78d11-118">Parameter.</span></span>

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

### <span data-ttu-id="78d11-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d11-119">-ResourceGroupName</span></span>
<span data-ttu-id="78d11-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78d11-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="78d11-121">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="78d11-121">-Section</span></span>
<span data-ttu-id="78d11-122">Bölümde.</span><span class="sxs-lookup"><span data-stu-id="78d11-122">Section.</span></span>

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

### <span data-ttu-id="78d11-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="78d11-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="78d11-124">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="78d11-124">Client authentication type.</span></span>

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

### <span data-ttu-id="78d11-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="78d11-125">-Confirm</span></span>
<span data-ttu-id="78d11-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78d11-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d11-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d11-127">-WhatIf</span></span>
<span data-ttu-id="78d11-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78d11-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78d11-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78d11-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d11-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d11-130">CommonParameters</span></span>
<span data-ttu-id="78d11-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78d11-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d11-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d11-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d11-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78d11-133">INPUTS</span></span>

### <span data-ttu-id="78d11-134">System. String</span><span class="sxs-lookup"><span data-stu-id="78d11-134">System.String</span></span>
<span data-ttu-id="78d11-135">Parametreler: Parameter (ByValue), Bölüm (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78d11-135">Parameters: Parameter (ByValue), Section (ByValue)</span></span>

### <span data-ttu-id="78d11-136">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="78d11-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="78d11-137">Parametreler: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78d11-137">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="78d11-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78d11-138">OUTPUTS</span></span>

### <span data-ttu-id="78d11-139">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="78d11-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="78d11-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78d11-140">NOTES</span></span>

## <span data-ttu-id="78d11-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78d11-141">RELATED LINKS</span></span>
