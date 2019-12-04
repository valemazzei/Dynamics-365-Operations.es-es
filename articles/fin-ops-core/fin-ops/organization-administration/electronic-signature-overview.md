---
title: Visión general de las firmas electrónicas
description: En este artículo se proporciona una visión general de las firmas electrónicas y se describe cómo pueden usarse.
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d1d8952324bb16bcfa6a8b42fc4f157edb75cf1
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811335"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="12ab6-103">Visión general de las firmas electrónicas</span><span class="sxs-lookup"><span data-stu-id="12ab6-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12ab6-104">En este artículo se proporciona una visión general de las firmas electrónicas y se describe cómo pueden usarse.</span><span class="sxs-lookup"><span data-stu-id="12ab6-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="12ab6-105">¿Qué es una firma electrónica?</span><span class="sxs-lookup"><span data-stu-id="12ab6-105">What is an electronic signature?</span></span>

<span data-ttu-id="12ab6-106">Una firma electrónica confirma la identidad de una persona que va a comenzar o aprobar un proceso informático.</span><span class="sxs-lookup"><span data-stu-id="12ab6-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="12ab6-107">En algunos sectores, una firma electrónica es tan vinculante legalmente como una firma escrita.</span><span class="sxs-lookup"><span data-stu-id="12ab6-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="12ab6-108">Las firmas electrónicas son un requisito de cumplimiento de directivas para determinados sectores regulados, como el farmacéutico, alimentación, aeroespacial y defensa.</span><span class="sxs-lookup"><span data-stu-id="12ab6-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="12ab6-109">También son necesarias para el cumplimiento de las directivas de 21 CFR Parte 11 que se publicaron por la Food and Drug Administration (FDA) en los Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="12ab6-110">Una firma electrónica por sí misma no es lo mismo que una firma digital.</span><span class="sxs-lookup"><span data-stu-id="12ab6-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="12ab6-111">Una firma electrónica es simplemente un sustituto de la firma manuscrita, mientras que una firma digital proporciona medidas de seguridad adicionales.</span><span class="sxs-lookup"><span data-stu-id="12ab6-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="12ab6-112">Una firma digital puede ayudar a identificar si otro usuario o proceso han manipulado los datos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="12ab6-113">Una firma digital también puede verificarse y esta verificación no la puede rechazar el propietario del certificado que se usó para firmar los datos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="12ab6-114">Como se describe a continuación, las firmas electrónicas han integrado la funcionalidad de la firma digital.</span><span class="sxs-lookup"><span data-stu-id="12ab6-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="12ab6-115">Firmas electrónicas</span><span class="sxs-lookup"><span data-stu-id="12ab6-115">Electronic signatures</span></span>

<span data-ttu-id="12ab6-116">Puede usar firmas electrónicas para procesos empresariales críticos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="12ab6-117">Algunos procesos llevan integrada la capacidad de firma electrónica.</span><span class="sxs-lookup"><span data-stu-id="12ab6-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="12ab6-118">También puede crear requisitos de firma personalizados para cualquier tabla o campo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="12ab6-119">Las firmas electrónicas han integrado la funcionalidad de la firma digital.</span><span class="sxs-lookup"><span data-stu-id="12ab6-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="12ab6-120">Cada usuario que firma documentos debe obtener un certificado criptográfico válido.</span><span class="sxs-lookup"><span data-stu-id="12ab6-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="12ab6-121">Cuando se firma un documento, se valida la clave privada que está asociada al certificado.</span><span class="sxs-lookup"><span data-stu-id="12ab6-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="12ab6-122">La información de firma electrónica se registra en un registro para proporcionar una traza de auditoría.</span><span class="sxs-lookup"><span data-stu-id="12ab6-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="12ab6-123">Para configurar las firmas electrónicas, consulte [Configuración de firmas electrónicas](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="12ab6-123">To set up electronic signatures, see [Set up electronic signatures](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="12ab6-124">Usuarios que requieren el acceso a las firmas electrónicas</span><span class="sxs-lookup"><span data-stu-id="12ab6-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="12ab6-125">Existen tres tipos de usuarios que necesitan normalmente acceso de seguridad a las firmas electrónicas: administradores de firma electrónica, firmantes y auditores de firma electrónica.</span><span class="sxs-lookup"><span data-stu-id="12ab6-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="12ab6-126">Administrador de firma electrónica</span><span class="sxs-lookup"><span data-stu-id="12ab6-126">Electronic signature administrator</span></span>

<span data-ttu-id="12ab6-127">El administrador de firma electrónica configura los requisitos de firma, configura los parámetros generales y los aprobadores, y recibe alertas cuando las firmas no se pueden verificar.</span><span class="sxs-lookup"><span data-stu-id="12ab6-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="12ab6-128">De forma predeterminada, un usuario que pertenezca al rol de seguridad **Director de tecnología de la información** tiene permiso para administrar las firmas electrónicas.</span><span class="sxs-lookup"><span data-stu-id="12ab6-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="12ab6-129">Firmante</span><span class="sxs-lookup"><span data-stu-id="12ab6-129">Signer</span></span>

<span data-ttu-id="12ab6-130">Un firmante proporciona firmas electrónicas para documentos y procesos que requieren firmas.</span><span class="sxs-lookup"><span data-stu-id="12ab6-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="12ab6-131">De forma predeterminada, un usuario que pertenezca al rol de seguridad **Usuario de sistema** tiene permiso para firmar documentos electrónicamente.</span><span class="sxs-lookup"><span data-stu-id="12ab6-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="12ab6-132">El firmante puede requerir permisos adicionales para que se conceda acceso a los datos que están relacionados con el documento o el proceso que se está firmando.</span><span class="sxs-lookup"><span data-stu-id="12ab6-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="12ab6-133">Un usuario que cambie datos y necesite firmar para validar los cambios, debe tener permiso para modificar los datos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="12ab6-134">Un usuario que firma en nombre de otro usuario quizás no requiera acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="12ab6-135">Un ejemplo de este tipo de usuario es un supervisor que firma para validar los cambios de un empleado.</span><span class="sxs-lookup"><span data-stu-id="12ab6-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="12ab6-136">Auditor de firma electrónica</span><span class="sxs-lookup"><span data-stu-id="12ab6-136">Electronic signature auditor</span></span>

<span data-ttu-id="12ab6-137">El auditor de firma electrónica revisa el registro de la base de datos y el registro de revisión de firma que está disponible en el registro de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="12ab6-138">De forma predeterminada, un usuario que pertenezca al rol de seguridad **Director de tecnología de la información** tiene permiso para auditar las firmas electrónicas.</span><span class="sxs-lookup"><span data-stu-id="12ab6-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="12ab6-139">Si usa un rol distinto de **Director de tecnología de la información**, asegúrese de que el rol tenga asignados los siguientes privilegios:</span><span class="sxs-lookup"><span data-stu-id="12ab6-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="12ab6-140">Ver errores de firmas electrónicas</span><span class="sxs-lookup"><span data-stu-id="12ab6-140">View electronic signature failures</span></span>
- <span data-ttu-id="12ab6-141">Ver registro de base de datos</span><span class="sxs-lookup"><span data-stu-id="12ab6-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="12ab6-142">Firmar documentos electrónicamente</span><span class="sxs-lookup"><span data-stu-id="12ab6-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="12ab6-143">Obtener un certificado</span><span class="sxs-lookup"><span data-stu-id="12ab6-143">Get a certificate</span></span>

<span data-ttu-id="12ab6-144">Antes de firmar documentos electrónicamente, debe solicitar un certificado.</span><span class="sxs-lookup"><span data-stu-id="12ab6-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="12ab6-145">Las características de Microsoft SQL Server se usan para crear certificados y permitir firmar electrónicamente.</span><span class="sxs-lookup"><span data-stu-id="12ab6-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="12ab6-146">No se requiere ningún certificado o infraestructura de clave pública (PKI) adicional.</span><span class="sxs-lookup"><span data-stu-id="12ab6-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="12ab6-147">Cuando solicita un certificado, se crea una clave pública y una clave privada para usted.</span><span class="sxs-lookup"><span data-stu-id="12ab6-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="12ab6-148">La clave privada se encripta mediante una contraseña que sólo usted conoce.</span><span class="sxs-lookup"><span data-stu-id="12ab6-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="12ab6-149">Cuando firma un documento electrónicamente, su identidad se verifica al introducir la contraseña.</span><span class="sxs-lookup"><span data-stu-id="12ab6-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="12ab6-150">Para solicitar un certificado, en la página **Opciones**, en la pestaña **Cuentas** , haga clic en **Obtener certificado**.</span><span class="sxs-lookup"><span data-stu-id="12ab6-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="12ab6-151">Debe escribir y confirmar la contraseña que usará para firmar.</span><span class="sxs-lookup"><span data-stu-id="12ab6-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="12ab6-152">La contraseña se usa para proteger su clave privada y autorizar el uso de su certificado.</span><span class="sxs-lookup"><span data-stu-id="12ab6-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="12ab6-153">Esta contraseña no se almacena en la base de datos y no está disponible para nadie, ni siquiera para el administrador.</span><span class="sxs-lookup"><span data-stu-id="12ab6-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="12ab6-154">Si olvida la contraseña conectada a su certificado, éste debe ser restablecido.</span><span class="sxs-lookup"><span data-stu-id="12ab6-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="12ab6-155">Si restablecer el certificado, no se verán afectados los documentos que haya firmado con el certificado anterior.</span><span class="sxs-lookup"><span data-stu-id="12ab6-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="12ab6-156">Para restablecer el certificado, en la página **Opciones**, haga clic en **Restablecer certificado**.</span><span class="sxs-lookup"><span data-stu-id="12ab6-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="12ab6-157">Firmar un documento electrónicamente</span><span class="sxs-lookup"><span data-stu-id="12ab6-157">Sign a document electronically</span></span>

<span data-ttu-id="12ab6-158">Cuando realice un cambio que requiera una firma electrónica se mostrará la página **Firmar documento**.</span><span class="sxs-lookup"><span data-stu-id="12ab6-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="12ab6-159">En la página **Firmar documento**, haga clic en la pestaña **Documento** para revisar las modificaciones del documento.</span><span class="sxs-lookup"><span data-stu-id="12ab6-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="12ab6-160">En la ficha **Firma**, seleccione un código de motivo.</span><span class="sxs-lookup"><span data-stu-id="12ab6-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="12ab6-161">Escriba un comentario, si se requiere uno.</span><span class="sxs-lookup"><span data-stu-id="12ab6-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="12ab6-162">Si su Id. de usuario no aparece en el campo **Firmante**, selecciónelo en la lista.</span><span class="sxs-lookup"><span data-stu-id="12ab6-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="12ab6-163">Escriba su ubicación, si esta información es necesaria.</span><span class="sxs-lookup"><span data-stu-id="12ab6-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="12ab6-164">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="12ab6-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="12ab6-165">Firmar por los cambios de otro usuario</span><span class="sxs-lookup"><span data-stu-id="12ab6-165">Sign for another user's changes</span></span>

<span data-ttu-id="12ab6-166">En ocasiones, puede querer que un usuario firme los cambios realizados por otro usuario.</span><span class="sxs-lookup"><span data-stu-id="12ab6-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="12ab6-167">Por ejemplo, puede que se requiera que un supervisor firme las modificaciones que determinados empleados realicen en las listas de materiales (L. MAT).</span><span class="sxs-lookup"><span data-stu-id="12ab6-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="12ab6-168">Use este procedimiento para designar un usuario como firmante por otro usuario.</span><span class="sxs-lookup"><span data-stu-id="12ab6-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="12ab6-169">Cuando un usuario firma por los cambios de otro, la firma debe proporcionarse en la estación de trabajo del usuario que realizó la modificación.</span><span class="sxs-lookup"><span data-stu-id="12ab6-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="12ab6-170">El usuario no puede guardar los cambios hasta que se proporcione la firma.</span><span class="sxs-lookup"><span data-stu-id="12ab6-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="12ab6-171">Para designar aprobadores, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="12ab6-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="12ab6-172">En la página **Opciones**, en la pestaña **Cuentas** , haga clic en **Designar aprobador**.</span><span class="sxs-lookup"><span data-stu-id="12ab6-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="12ab6-173">En el campo **Id. del aprobador**, seleccione el Id. del usuario que debe firmar por los cambios de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="12ab6-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="12ab6-174">En el campo **Firmar para id. de usuario**, seleccione el Id. del usuario cuyos cambios deberán firmarse.</span><span class="sxs-lookup"><span data-stu-id="12ab6-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>