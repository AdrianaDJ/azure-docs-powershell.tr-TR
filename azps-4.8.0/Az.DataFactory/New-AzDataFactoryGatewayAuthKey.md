---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267799"
---
# <span data-ttu-id="b90d6-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="b90d6-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="b90d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b90d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b90d6-103">Azure Data Factory ağ geçidi için auth anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b90d6-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="b90d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b90d6-104">SYNTAX</span></span>

### <span data-ttu-id="b90d6-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b90d6-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b90d6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b90d6-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b90d6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b90d6-107">DESCRIPTION</span></span>
<span data-ttu-id="b90d6-108">**Yeni-Azverifactorygatewaygatewaykey** cmdlet 'i, belirli bir Azure Data Factory ağ geçidi için ağ geçidi doğrulama anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b90d6-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="b90d6-109">Bu anahtarı kullanarak ağ geçidini bir bulut hizmetiyle kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="b90d6-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="b90d6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b90d6-110">EXAMPLES</span></span>

### <span data-ttu-id="b90d6-111">Örnek 1: anahtar için bir ağ geçidi kimlik doğrulama anahtarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="b90d6-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="b90d6-112">Bu komut MyGateway adlı Data Factory ağ geçidi için anahtar için bir Gateway auth anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b90d6-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="b90d6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b90d6-113">PARAMETERS</span></span>

### <span data-ttu-id="b90d6-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b90d6-114">-DataFactoryName</span></span>
<span data-ttu-id="b90d6-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="b90d6-115">The data factory name.</span></span>

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

### <span data-ttu-id="b90d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90d6-116">-DefaultProfile</span></span>
<span data-ttu-id="b90d6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b90d6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b90d6-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="b90d6-118">-GatewayName</span></span>
<span data-ttu-id="b90d6-119">Veri Fabrikası ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="b90d6-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="b90d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b90d6-120">-InputObject</span></span>
<span data-ttu-id="b90d6-121">Veri fabrikası nesnesi</span><span class="sxs-lookup"><span data-stu-id="b90d6-121">The data factory object</span></span>

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

### <span data-ttu-id="b90d6-122">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="b90d6-122">-KeyName</span></span>
<span data-ttu-id="b90d6-123">' Anahtar ' veya ' anahtar2 ' yeniden üretilecek Ağ Geçidi kimlik doğrulama anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="b90d6-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="b90d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="b90d6-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b90d6-125">The resource group name.</span></span>

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

### <span data-ttu-id="b90d6-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b90d6-126">-Confirm</span></span>
<span data-ttu-id="b90d6-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b90d6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b90d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90d6-128">-WhatIf</span></span>
<span data-ttu-id="b90d6-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b90d6-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b90d6-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b90d6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b90d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90d6-131">CommonParameters</span></span>
<span data-ttu-id="b90d6-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b90d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90d6-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90d6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90d6-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b90d6-134">INPUTS</span></span>

### <span data-ttu-id="b90d6-135">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="b90d6-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b90d6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b90d6-136">System.String</span></span>

## <span data-ttu-id="b90d6-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b90d6-137">OUTPUTS</span></span>

### <span data-ttu-id="b90d6-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="b90d6-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="b90d6-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b90d6-139">NOTES</span></span>
* <span data-ttu-id="b90d6-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="b90d6-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b90d6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b90d6-141">RELATED LINKS</span></span>

<span data-ttu-id="b90d6-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-Azdatafactorygatewaygatewaykey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="b90d6-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

