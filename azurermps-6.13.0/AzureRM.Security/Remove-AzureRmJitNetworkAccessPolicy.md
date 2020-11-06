---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589346"
---
# <span data-ttu-id="388f1-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="388f1-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="388f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="388f1-102">SYNOPSIS</span></span>
<span data-ttu-id="388f1-103">Bir JıT ağ erişim ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="388f1-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="388f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="388f1-104">SYNTAX</span></span>

### <span data-ttu-id="388f1-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="388f1-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="388f1-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="388f1-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="388f1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="388f1-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="388f1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="388f1-108">DESCRIPTION</span></span>
<span data-ttu-id="388f1-109">Bir kerelik ağ erişim ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="388f1-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="388f1-110">Bu eylemden sonra, Kullanıcı silinen ilke içinde yapılandırılmış VM 'lerde geçici ağ bağlantısı istemeyecektir.</span><span class="sxs-lookup"><span data-stu-id="388f1-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="388f1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="388f1-111">EXAMPLES</span></span>

### <span data-ttu-id="388f1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="388f1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="388f1-113">Bir kerelik ağ erişim ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="388f1-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="388f1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="388f1-114">PARAMETERS</span></span>

### <span data-ttu-id="388f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388f1-115">-DefaultProfile</span></span>
<span data-ttu-id="388f1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="388f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="388f1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="388f1-117">-InputObject</span></span>
<span data-ttu-id="388f1-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="388f1-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="388f1-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="388f1-119">-Location</span></span>
<span data-ttu-id="388f1-120">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="388f1-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388f1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="388f1-121">-Name</span></span>
<span data-ttu-id="388f1-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="388f1-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388f1-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="388f1-123">-PassThru</span></span>
<span data-ttu-id="388f1-124">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="388f1-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="388f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="388f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="388f1-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="388f1-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388f1-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="388f1-127">-ResourceId</span></span>
<span data-ttu-id="388f1-128">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="388f1-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388f1-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="388f1-129">-Confirm</span></span>
<span data-ttu-id="388f1-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="388f1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388f1-131">-WhatIf</span></span>
<span data-ttu-id="388f1-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="388f1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="388f1-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="388f1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388f1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388f1-134">CommonParameters</span></span>
<span data-ttu-id="388f1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="388f1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388f1-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388f1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388f1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="388f1-137">INPUTS</span></span>

### <span data-ttu-id="388f1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="388f1-138">System.String</span></span>
<span data-ttu-id="388f1-139">Microsoft. Azure. Commands. Security. cmdlet. Jnetworkaccesspolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="388f1-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="388f1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="388f1-140">OUTPUTS</span></span>

### <span data-ttu-id="388f1-141">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="388f1-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="388f1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="388f1-142">NOTES</span></span>

## <span data-ttu-id="388f1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="388f1-143">RELATED LINKS</span></span>
