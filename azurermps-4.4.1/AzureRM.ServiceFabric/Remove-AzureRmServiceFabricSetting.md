---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 6fe4d0c3a32cd96693d64e46f9d8596083dd9c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589089"
---
# <span data-ttu-id="ad9a5-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ad9a5-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="ad9a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9a5-103">Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad9a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad9a5-104">SYNTAX</span></span>

### <span data-ttu-id="ad9a5-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="ad9a5-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad9a5-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="ad9a5-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad9a5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad9a5-107">DESCRIPTION</span></span>
<span data-ttu-id="ad9a5-108">Kümeden hizmet doku ayarlarını kaldırmak için **Remove-AzureRmServiceFabricSetting** 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="ad9a5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad9a5-109">EXAMPLES</span></span>

### <span data-ttu-id="ad9a5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ad9a5-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="ad9a5-111">Bu komut ' eseslerer'</span><span class="sxs-lookup"><span data-stu-id="ad9a5-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="ad9a5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad9a5-112">PARAMETERS</span></span>

### <span data-ttu-id="ad9a5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad9a5-113">-Name</span></span>
<span data-ttu-id="ad9a5-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ad9a5-115">-Parametre</span><span class="sxs-lookup"><span data-stu-id="ad9a5-115">-Parameter</span></span>
<span data-ttu-id="ad9a5-116">Parametresi.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-116">Parameter.</span></span>

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

### <span data-ttu-id="ad9a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad9a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad9a5-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ad9a5-119">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="ad9a5-119">-Section</span></span>
<span data-ttu-id="ad9a5-120">Bölümde.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-120">Section.</span></span>

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

### <span data-ttu-id="ad9a5-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="ad9a5-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="ad9a5-122">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-122">Client authentication type.</span></span>

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

### <span data-ttu-id="ad9a5-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad9a5-123">-Confirm</span></span>
<span data-ttu-id="ad9a5-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad9a5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9a5-125">-WhatIf</span></span>
<span data-ttu-id="ad9a5-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad9a5-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad9a5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9a5-128">-DefaultProfile</span></span>
<span data-ttu-id="ad9a5-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad9a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9a5-130">CommonParameters</span></span>
<span data-ttu-id="ad9a5-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad9a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9a5-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad9a5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9a5-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad9a5-133">INPUTS</span></span>

### <span data-ttu-id="ad9a5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ad9a5-134">System.String</span></span>
<span data-ttu-id="ad9a5-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="ad9a5-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="ad9a5-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad9a5-136">OUTPUTS</span></span>

### <span data-ttu-id="ad9a5-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="ad9a5-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="ad9a5-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad9a5-138">NOTES</span></span>

## <span data-ttu-id="ad9a5-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad9a5-139">RELATED LINKS</span></span>

