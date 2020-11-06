---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589769"
---
# <span data-ttu-id="e5e1c-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="e5e1c-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="e5e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e1c-103">Azure IoT Hub sertifikasını siler.</span><span class="sxs-lookup"><span data-stu-id="e5e1c-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5e1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5e1c-104">SYNTAX</span></span>

### <span data-ttu-id="e5e1c-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5e1c-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e1c-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="e5e1c-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e1c-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e5e1c-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e1c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e1c-109">Azure IoT Hub 'daki CA sertifikalarının ayrıntılı açıklaması için bkz: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="e5e1c-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="e5e1c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="e5e1c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5e1c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="e5e1c-112">Sertifikamı silme</span><span class="sxs-lookup"><span data-stu-id="e5e1c-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="e5e1c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5e1c-113">PARAMETERS</span></span>

### <span data-ttu-id="e5e1c-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e5e1c-114">-CertificateName</span></span>
<span data-ttu-id="e5e1c-115">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="e5e1c-115">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e1c-116">-DefaultProfile</span></span>
<span data-ttu-id="e5e1c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5e1c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="e5e1c-118">-Etag</span></span>
<span data-ttu-id="e5e1c-119">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="e5e1c-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e1c-120">-InputObject</span></span>
<span data-ttu-id="e5e1c-121">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="e5e1c-121">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5e1c-122">-Name</span></span>
<span data-ttu-id="e5e1c-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="e5e1c-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e5e1c-124">-PassThru</span></span>
<span data-ttu-id="e5e1c-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="e5e1c-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e1c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5e1c-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e5e1c-127">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e5e1c-128">-ResourceId</span></span>
<span data-ttu-id="e5e1c-129">Sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e5e1c-129">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5e1c-130">-Confirm</span></span>
<span data-ttu-id="e5e1c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5e1c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e1c-132">-WhatIf</span></span>
<span data-ttu-id="e5e1c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5e1c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e1c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5e1c-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e1c-135">CommonParameters</span></span>
<span data-ttu-id="e5e1c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5e1c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e1c-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e1c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e1c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5e1c-138">INPUTS</span></span>

### <span data-ttu-id="e5e1c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e1c-139">System.String</span></span>

## <span data-ttu-id="e5e1c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5e1c-140">OUTPUTS</span></span>

### <span data-ttu-id="e5e1c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5e1c-141">System.Boolean</span></span>

## <span data-ttu-id="e5e1c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5e1c-142">NOTES</span></span>

## <span data-ttu-id="e5e1c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5e1c-143">RELATED LINKS</span></span>

