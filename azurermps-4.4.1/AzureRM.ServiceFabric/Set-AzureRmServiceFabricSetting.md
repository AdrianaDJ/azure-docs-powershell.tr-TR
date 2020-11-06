---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: ef369f67e683a214538f1ecb113f771e2f5cd2f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589088"
---
# <span data-ttu-id="67b75-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="67b75-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="67b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b75-102">SYNOPSIS</span></span>
<span data-ttu-id="67b75-103">Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="67b75-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67b75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67b75-104">SYNTAX</span></span>

### <span data-ttu-id="67b75-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="67b75-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67b75-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="67b75-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b75-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="67b75-107">DESCRIPTION</span></span>
<span data-ttu-id="67b75-108">Kümeye hizmet yapısı ayarları eklemek veya bunları güncelleştirmek için **set-AzureRmServiceFabricSetting** kullanın.</span><span class="sxs-lookup"><span data-stu-id="67b75-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="67b75-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67b75-109">EXAMPLES</span></span>

### <span data-ttu-id="67b75-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67b75-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="67b75-111">Bu komut, ' NamingService ' bölümünün altındaki ' MaxFileOperationTimeout ' değerini ' 5000 ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="67b75-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="67b75-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67b75-112">PARAMETERS</span></span>

### <span data-ttu-id="67b75-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="67b75-113">-Name</span></span>
<span data-ttu-id="67b75-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="67b75-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="67b75-115">-Parametre</span><span class="sxs-lookup"><span data-stu-id="67b75-115">-Parameter</span></span>
<span data-ttu-id="67b75-116">Parametresi.</span><span class="sxs-lookup"><span data-stu-id="67b75-116">Parameter.</span></span>

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

### <span data-ttu-id="67b75-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b75-117">-ResourceGroupName</span></span>
<span data-ttu-id="67b75-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67b75-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="67b75-119">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="67b75-119">-Section</span></span>
<span data-ttu-id="67b75-120">Bölümde.</span><span class="sxs-lookup"><span data-stu-id="67b75-120">Section.</span></span>

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

### <span data-ttu-id="67b75-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="67b75-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="67b75-122">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="67b75-122">Client authentication type.</span></span>

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

### <span data-ttu-id="67b75-123">-Değer</span><span class="sxs-lookup"><span data-stu-id="67b75-123">-Value</span></span>
<span data-ttu-id="67b75-124">Değerlerini.</span><span class="sxs-lookup"><span data-stu-id="67b75-124">Value.</span></span>

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

### <span data-ttu-id="67b75-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="67b75-125">-Confirm</span></span>
<span data-ttu-id="67b75-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67b75-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b75-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67b75-127">-WhatIf</span></span>
<span data-ttu-id="67b75-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67b75-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67b75-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67b75-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67b75-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b75-130">-DefaultProfile</span></span>
<span data-ttu-id="67b75-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67b75-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67b75-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b75-132">CommonParameters</span></span>
<span data-ttu-id="67b75-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67b75-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b75-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b75-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b75-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67b75-135">INPUTS</span></span>

### <span data-ttu-id="67b75-136">System. String</span><span class="sxs-lookup"><span data-stu-id="67b75-136">System.String</span></span>
<span data-ttu-id="67b75-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="67b75-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="67b75-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67b75-138">OUTPUTS</span></span>

### <span data-ttu-id="67b75-139">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="67b75-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="67b75-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67b75-140">NOTES</span></span>

## <span data-ttu-id="67b75-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67b75-141">RELATED LINKS</span></span>

