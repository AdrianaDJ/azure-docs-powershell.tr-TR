---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7ec2ac54f6fc212dba11a0c761dd0f9d76a6ee53
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936687"
---
# <span data-ttu-id="57ede-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="57ede-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="57ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ede-102">SYNOPSIS</span></span>
<span data-ttu-id="57ede-103">Azure IoT Hub anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="57ede-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="57ede-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57ede-104">SYNTAX</span></span>

### <span data-ttu-id="57ede-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57ede-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57ede-106">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="57ede-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57ede-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="57ede-107">DESCRIPTION</span></span>
<span data-ttu-id="57ede-108">Azure IoT Hub anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="57ede-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="57ede-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57ede-109">EXAMPLES</span></span>

### <span data-ttu-id="57ede-110">Örnek 1 birincil anahtarı yeniden üret</span><span class="sxs-lookup"><span data-stu-id="57ede-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="57ede-111">Azure IoT Hub 'ının "testKey" yetkilendirme ilkesi için birincil anahtar yeniden oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="57ede-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="57ede-112">Örnek 2 takas tuşları</span><span class="sxs-lookup"><span data-stu-id="57ede-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="57ede-113">Azure IoT Hub 'ının "testKey" yetkilendirme ilkesi için anahtar değiştirme.</span><span class="sxs-lookup"><span data-stu-id="57ede-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="57ede-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57ede-114">PARAMETERS</span></span>

### <span data-ttu-id="57ede-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ede-115">-DefaultProfile</span></span>
<span data-ttu-id="57ede-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="57ede-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57ede-117">-Hubıd</span><span class="sxs-lookup"><span data-stu-id="57ede-117">-HubId</span></span>
<span data-ttu-id="57ede-118">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="57ede-118">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ede-119">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="57ede-119">-KeyName</span></span>
<span data-ttu-id="57ede-120">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="57ede-120">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ede-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="57ede-121">-Name</span></span>
<span data-ttu-id="57ede-122">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="57ede-122">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ede-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="57ede-123">-RenewKey</span></span>
<span data-ttu-id="57ede-124">Anahtarı yeniden üret.</span><span class="sxs-lookup"><span data-stu-id="57ede-124">Regenerate Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ede-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ede-125">-ResourceGroupName</span></span>
<span data-ttu-id="57ede-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="57ede-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ede-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="57ede-127">-Confirm</span></span>
<span data-ttu-id="57ede-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57ede-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ede-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ede-129">-WhatIf</span></span>
<span data-ttu-id="57ede-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57ede-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ede-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57ede-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ede-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ede-132">CommonParameters</span></span>
<span data-ttu-id="57ede-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57ede-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ede-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ede-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ede-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57ede-135">INPUTS</span></span>

### <span data-ttu-id="57ede-136">System. String</span><span class="sxs-lookup"><span data-stu-id="57ede-136">System.String</span></span>

## <span data-ttu-id="57ede-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57ede-137">OUTPUTS</span></span>

### <span data-ttu-id="57ede-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="57ede-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="57ede-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57ede-139">NOTES</span></span>

## <span data-ttu-id="57ede-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57ede-140">RELATED LINKS</span></span>