---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 38c937de07d4a19a6c2632356c2b9ac58b2b416a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104170"
---
# <span data-ttu-id="b1f6f-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b1f6f-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="b1f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f6f-103">Bir API yönetim özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="b1f6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1f6f-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f6f-106">**Set-Azapsananagementproperty** cmdlet 'ı BIR Azure API yönetim özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="b1f6f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1f6f-107">EXAMPLES</span></span>

### <span data-ttu-id="b1f6f-108">Örnek 1: bir özellikte etiketleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="b1f6f-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="b1f6f-109">İlk komut $Tags değişkenine iki değer atar.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="b1f6f-110">İkinci komut Property11 KIMLIĞINE sahip özelliği değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="b1f6f-111">Komut, $Tags dizeleri özellik üzerinde etiket olarak atar.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="b1f6f-112">Örnek 2: bir özelliği gizli değeri olacak şekilde değiştirme</span><span class="sxs-lookup"><span data-stu-id="b1f6f-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="b1f6f-113">Bu komut, özelliği şifrelenecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="b1f6f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1f6f-114">PARAMETERS</span></span>

### <span data-ttu-id="b1f6f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b1f6f-115">-Context</span></span>
<span data-ttu-id="b1f6f-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f6f-117">-DefaultProfile</span></span>
<span data-ttu-id="b1f6f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1f6f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1f6f-119">-Name</span></span>
<span data-ttu-id="b1f6f-120">Özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-120">Specifies the name of the property.</span></span>
<span data-ttu-id="b1f6f-121">Maksimum Uzunluk 100 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="b1f6f-122">Adlar yalnızca harf, rakam, nokta, çizgi ve alt çizgi karakterlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f6f-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b1f6f-123">-PassThru</span></span>
<span data-ttu-id="b1f6f-124">Bu cmdlet 'in değiştirdiği **Psapsananagementözelliğini** geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f6f-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="b1f6f-125">-PropertyId</span></span>
<span data-ttu-id="b1f6f-126">Bu cmdlet 'in değiştirdiği özelliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f6f-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="b1f6f-127">-Secret</span></span>
<span data-ttu-id="b1f6f-128">Özellik değerinin gizli olduğunu ve şifrelenmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f6f-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b1f6f-129">-Tag</span></span>
<span data-ttu-id="b1f6f-130">Bir özellikle ilişkilendirilmiş Etiketler.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-130">Tags associated with a property.</span></span> <span data-ttu-id="b1f6f-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-131">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f6f-132">-Değer</span><span class="sxs-lookup"><span data-stu-id="b1f6f-132">-Value</span></span>
<span data-ttu-id="b1f6f-133">Özellik için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-133">Specifies a value for the property.</span></span>
<span data-ttu-id="b1f6f-134">Bu değer ilke ifadeleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="b1f6f-135">Maksimum uzunluk 1000 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="b1f6f-136">Değer boş olamaz veya yalnızca boşluklardan oluşamaz.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-136">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f6f-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1f6f-137">-Confirm</span></span>
<span data-ttu-id="b1f6f-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f6f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f6f-139">-WhatIf</span></span>
<span data-ttu-id="b1f6f-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1f6f-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f6f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f6f-142">CommonParameters</span></span>
<span data-ttu-id="b1f6f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f6f-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b1f6f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f6f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1f6f-145">INPUTS</span></span>

### <span data-ttu-id="b1f6f-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="b1f6f-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1f6f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f6f-147">System.String</span></span>

### <span data-ttu-id="b1f6f-148">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b1f6f-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b1f6f-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="b1f6f-149">System.String[]</span></span>

### <span data-ttu-id="b1f6f-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b1f6f-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b1f6f-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1f6f-151">OUTPUTS</span></span>

### <span data-ttu-id="b1f6f-152">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="b1f6f-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="b1f6f-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1f6f-153">NOTES</span></span>

## <span data-ttu-id="b1f6f-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1f6f-154">RELATED LINKS</span></span>

[<span data-ttu-id="b1f6f-155">Get-Azapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="b1f6f-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="b1f6f-156">New-Azapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="b1f6f-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="b1f6f-157">Remove-Azapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="b1f6f-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


