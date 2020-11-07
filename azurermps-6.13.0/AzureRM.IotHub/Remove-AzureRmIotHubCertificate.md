---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: de24d9d16af5b429dcf59ffc8f4cbeb7dd0654f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762719"
---
# <span data-ttu-id="ad523-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="ad523-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="ad523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad523-102">SYNOPSIS</span></span>
<span data-ttu-id="ad523-103">Azure IoT Hub sertifikasını siler.</span><span class="sxs-lookup"><span data-stu-id="ad523-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad523-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad523-104">SYNTAX</span></span>

### <span data-ttu-id="ad523-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad523-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad523-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="ad523-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad523-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="ad523-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad523-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad523-108">DESCRIPTION</span></span>
<span data-ttu-id="ad523-109">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="ad523-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="ad523-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad523-110">EXAMPLES</span></span>

### <span data-ttu-id="ad523-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ad523-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="ad523-112">Sertifikamı silme</span><span class="sxs-lookup"><span data-stu-id="ad523-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="ad523-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad523-113">PARAMETERS</span></span>

### <span data-ttu-id="ad523-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ad523-114">-CertificateName</span></span>
<span data-ttu-id="ad523-115">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="ad523-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad523-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad523-116">-DefaultProfile</span></span>
<span data-ttu-id="ad523-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad523-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad523-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="ad523-118">-Etag</span></span>
<span data-ttu-id="ad523-119">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="ad523-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad523-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad523-120">-InputObject</span></span>
<span data-ttu-id="ad523-121">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="ad523-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad523-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad523-122">-Name</span></span>
<span data-ttu-id="ad523-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="ad523-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ad523-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ad523-124">-PassThru</span></span>
<span data-ttu-id="ad523-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ad523-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad523-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad523-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad523-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ad523-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ad523-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ad523-128">-ResourceId</span></span>
<span data-ttu-id="ad523-129">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ad523-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="ad523-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad523-130">-Confirm</span></span>
<span data-ttu-id="ad523-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad523-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad523-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad523-132">-WhatIf</span></span>
<span data-ttu-id="ad523-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad523-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad523-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad523-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad523-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad523-135">CommonParameters</span></span>
<span data-ttu-id="ad523-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad523-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad523-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad523-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad523-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad523-138">INPUTS</span></span>

### <span data-ttu-id="ad523-139">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscercertificate Atedescription</span><span class="sxs-lookup"><span data-stu-id="ad523-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="ad523-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad523-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ad523-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad523-141">System.String</span></span>

## <span data-ttu-id="ad523-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad523-142">OUTPUTS</span></span>

### <span data-ttu-id="ad523-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad523-143">System.Boolean</span></span>

## <span data-ttu-id="ad523-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad523-144">NOTES</span></span>

## <span data-ttu-id="ad523-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad523-145">RELATED LINKS</span></span>
