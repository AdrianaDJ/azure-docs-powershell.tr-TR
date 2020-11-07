---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: b7f435090c0ff5c421df7d8d3e885f67456f9af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764146"
---
# <span data-ttu-id="edb8c-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="edb8c-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="edb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="edb8c-103">Azure Data Factory ağ geçidi için auth anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edb8c-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edb8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edb8c-104">SYNTAX</span></span>

### <span data-ttu-id="edb8c-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="edb8c-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edb8c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="edb8c-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb8c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="edb8c-107">DESCRIPTION</span></span>
<span data-ttu-id="edb8c-108">**Yeni-AzureRmDataFactoryGatewayAuthKey** cmdlet 'i, belirli bir Azure Data Factory ağ geçidi için ağ geçidi doğrulama anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edb8c-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="edb8c-109">Bu anahtarı kullanarak ağ geçidini bir bulut hizmetiyle kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="edb8c-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="edb8c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edb8c-110">EXAMPLES</span></span>

### <span data-ttu-id="edb8c-111">Örnek 1: anahtar için bir ağ geçidi kimlik doğrulama anahtarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="edb8c-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="edb8c-112">Bu komut MyGateway adlı Data Factory ağ geçidi için anahtar için bir Gateway auth anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edb8c-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="edb8c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edb8c-113">PARAMETERS</span></span>

### <span data-ttu-id="edb8c-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="edb8c-114">-DataFactoryName</span></span>
<span data-ttu-id="edb8c-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="edb8c-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb8c-116">-DefaultProfile</span></span>
<span data-ttu-id="edb8c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="edb8c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edb8c-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="edb8c-118">-GatewayName</span></span>
<span data-ttu-id="edb8c-119">Veri Fabrikası ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="edb8c-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="edb8c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edb8c-120">-InputObject</span></span>
<span data-ttu-id="edb8c-121">Veri fabrikası nesnesi</span><span class="sxs-lookup"><span data-stu-id="edb8c-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edb8c-122">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="edb8c-122">-KeyName</span></span>
<span data-ttu-id="edb8c-123">' Anahtar ' veya ' anahtar2 ' yeniden üretilecek Ağ Geçidi kimlik doğrulama anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="edb8c-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="edb8c-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="edb8c-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb8c-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="edb8c-126">-Confirm</span></span>
<span data-ttu-id="edb8c-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edb8c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb8c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb8c-128">-WhatIf</span></span>
<span data-ttu-id="edb8c-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edb8c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edb8c-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edb8c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb8c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb8c-131">CommonParameters</span></span>
<span data-ttu-id="edb8c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edb8c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb8c-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb8c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb8c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edb8c-134">INPUTS</span></span>

### <span data-ttu-id="edb8c-135">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="edb8c-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="edb8c-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="edb8c-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="edb8c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="edb8c-137">System.String</span></span>

## <span data-ttu-id="edb8c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edb8c-138">OUTPUTS</span></span>

### <span data-ttu-id="edb8c-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="edb8c-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="edb8c-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edb8c-140">NOTES</span></span>
* <span data-ttu-id="edb8c-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="edb8c-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="edb8c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edb8c-142">RELATED LINKS</span></span>

<span data-ttu-id="edb8c-143">[Yeni-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="edb8c-143">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

